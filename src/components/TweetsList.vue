<template>
    <div>
      <div v-for="tweet in tweets" :key="tweet.id" class="tweet">
        <hr class="border-gray-600">
        <div class="flex flex-shrink-0 p-4 pb-0">
          <a href="#" class="flex-shrink-0 group block">
            <div class="flex items-center">
                <UserProfil :profile_image="profile_image"/>
              <div class="ml-3">
                <p class="text-base leading-6 font-medium ">
                  {{ tweet.user.name }}
                  <span class="text-sm leading-5 font-medium text-gray-400 group-hover:text-gray-300 transition ease-in-out duration-150">
                    {{ tweet.user.handle }} . {{ tweet.time }}
                  </span>
                </p>
              </div>
            </div>
          </a>
        </div>
        <div class="pl-16">
          <p class="text-base width-auto font-medium flex-shrink">
            {{ tweet.content }}
          </p>
        </div>
        <IconsTweets />
      </div>
    </div>
  </template>
  
  <script>
  import axios from 'axios';
  import UserProfil from './UserProfil.vue';
  import IconsTweets from './IconsTweets.vue';
  
  export default {
    name: "TweetsList",
    components: {
      UserProfil,
      IconsTweets
    },
    data() {
      return {
        tweets: [],
        profile_image:"https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT9gg6fq8rAKIeKQKcR-h-Y-XAfesKlN_iQ4Q&s"

      };
    },
    mounted() {
      // Faire la requête pour récupérer les tweets et les utilisateurs
      axios.all([
        axios.get('http://localhost:3000/tweets'),
        axios.get('http://localhost:3000/users')
      ])
      .then(axios.spread((tweetsResponse, usersResponse) => {
        // Associer les utilisateurs aux tweets
        this.tweets = tweetsResponse.data.map(tweet => {
          const user = usersResponse.data.find(user => user.id === tweet.userId);
          tweet.user = user;
          tweet.time = new Date(tweet.createdAt).toLocaleTimeString([], { hour: '2-digit', minute: '2-digit' });
          return tweet;
        });
      }))
      .catch(error => {
        console.error('Erreur lors de la récupération des données :', error);
      });
    }
  };
  </script>
  
  <style>
  /* Ajoutez vos styles ici */
  </style>
  