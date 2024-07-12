<template>
  <div>
    <div class="flex-1 px-2 pt-2  relative">
        <input type="text" class="bg-gray-200 rounded-full border text-gray-400 h-9 font-medium text-lg w-full pl-6" placeholder="Search Twitter">
        <svg class="absolute left-4 top-7 transform -translate-y-1/2 text-gray-400" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor" width="20" height="20">
        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M10 4a6 6 0 00-4.546 9.664l-4.243 4.242a1 1 0 001.414 1.414l4.243-4.243A6 6 0 1010 4z"/>
        </svg>
    </div>
    <div class="bg-gray-100 rounded-lg p-2 mt-2">
      <div class="flex">
  <h2 class="font-bold">Suggestions pour vous</h2>
  <svg class="ml-24 text-gray-500 text-blue-600" xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24">
    <path fill="text-blue-600" fill-rule="evenodd" d="M12.563 3.2h-1.126l-.645 2.578l-.647.2a6.3 6.3 0 0 0-1.091.452l-.599.317l-2.28-1.368l-.796.797l1.368 2.28l-.317.598a6.3 6.3 0 0 0-.453 1.091l-.199.647l-2.578.645v1.126l2.578.645l.2.647q.173.568.452 1.091l.317.599l-1.368 2.28l.797.796l2.28-1.368l.598.317q.523.278 1.091.453l.647.199l.645 2.578h1.126l.645-2.578l.647-.2a6.3 6.3 0 0 0 1.091-.452l.599-.317l2.28 1.368l.796-.797l-1.368-2.28l.317-.598q.278-.523.453-1.091l.199-.647l2.578-.645v-1.126l-2.578-.645l-.2-.647a6.3 6.3 0 0 0-.452-1.091l-.317-.599l1.368-2.28l-.797-.796l-2.28 1.368l-.598-.317a6.3 6.3 0 0 0-1.091-.453l-.647-.199zm2.945 2.17l1.833-1.1a1 1 0 0 1 1.221.15l1.018 1.018a1 1 0 0 1 .15 1.221l-1.1 1.833q.33.62.54 1.3l2.073.519a1 1 0 0 1 .757.97v1.438a1 1 0 0 1-.757.97l-2.073.519q-.21.68-.54 1.3l1.1 1.833a1 1 0 0 1-.15 1.221l-1.018 1.018a1 1 0 0 1-1.221.15l-1.833-1.1q-.62.33-1.3.54l-.519 2.073a1 1 0 0 1-.97.757h-1.438a1 1 0 0 1-.97-.757l-.519-2.073a7.5 7.5 0 0 1-1.3-.54l-1.833 1.1a1 1 0 0 1-1.221-.15L4.42 18.562a1 1 0 0 1-.15-1.221l1.1-1.833a7.5 7.5 0 0 1-.54-1.3l-2.073-.519A1 1 0 0 1 2 12.72v-1.438a1 1 0 0 1 .757-.97l2.073-.519q.21-.68.54-1.3L4.27 6.66a1 1 0 0 1 .15-1.221L5.438 4.42a1 1 0 0 1 1.221-.15l1.833 1.1q.62-.33 1.3-.54l.519-2.073A1 1 0 0 1 11.28 2h1.438a1 1 0 0 1 .97.757l.519 2.073q.68.21 1.3.54zM12 14.8a2.8 2.8 0 1 0 0-5.6a2.8 2.8 0 0 0 0 5.6m0 1.2a4 4 0 1 1 0-8a4 4 0 0 1 0 8"/>
  </svg>
  </div>
  
      
               
                     <TrendTweet />
                     <div class="flex">
                        <div class="flex-1 p-4">
                            <h2 class="px-4 ml-2 w-48 font-bold text-blue-400">Show more</h2>  
                        </div>
                    </div>

                <!--third-people suggetion to follow section-->
                
            
                    <div class="flex">
                        <div class="flex-1 m-2">
                            <h2 class="px-4 py-2 text-xl w-48 font-semibold ">Who to follow</h2>
                        </div>
                    </div>
                        
                

                      <FollowPerson/>
                    
          
                 
                    <div class="flex">
                        <div class="flex-1 p-4">
                            <h2 class="px-4 ml-2 w-48 font-bold text-blue-400">Show more</h2>  
                        </div>
                    </div>

            
        </div>

</div>


    <!-- <ul>
      <li v-for="user in suggestedUsers" :key="user.id">
        <div>{{ user.username }}</div>
        <button>Suivre</button>
      </li>
    </ul> -->
  
  
</template>

<script>
import TrendTweet from './TrendTweet.vue';
import FollowPerson from './FollowPerson.vue';
export default {
  components:{
    TrendTweet,
    FollowPerson
  },
  data() {
    return {
      suggestedUsers: [] // Données des utilisateurs suggérés seront récupérées depuis JSON Server
    }
  },
  // Méthodes pour récupérer les utilisateurs suggérés depuis JSON Server
}
</script>

<style scoped>
/* Styles Tailwind CSS personnalisés pour les suggestions d'utilisateurs */
</style>
