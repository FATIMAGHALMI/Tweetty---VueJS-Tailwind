<template>

    <div class=" border border-gray-400 h-auto   border-t-0">
                <HomeHeader />
                <hr class="border-gray-400">
                <div class="flex mt-2">
                    <UserProfil :profile_image="profile_image"/>
                        <HomeSearch />            
                </div>
                <hr class="border-gray-400 border-3">
                <TweetsList />
                
                
    </div>


</template>

<script>
import HomeHeader from './HomeHeader.vue';
import UserProfil from './UserProfil.vue';
import HomeSearch from './HomeSearch.vue';
import TweetsList from './TweetsList.vue';

export default {
    components: {
    HomeHeader,
    UserProfil,
    HomeSearch,
    TweetsList,
   
  },
  data(){
    return{
        profile_image:"https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT9gg6fq8rAKIeKQKcR-h-Y-XAfesKlN_iQ4Q&s"
    }
  }

}
</script>

<style >

</style>
