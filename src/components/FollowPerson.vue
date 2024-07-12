<template>
    <div>
      <div v-for="user in suggestedUsers" :key="user.id" class="follow-item flex items-center justify-between p-4">
        <div class="flex items-center">
          <img :src="user.profileImage" alt="Profile Image" class="w-10 h-10 rounded-full">
          <div class="ml-4">
            <p class="font-bold">{{ user.name }}</p>
            <p class="text-gray-500">{{ user.handle }}</p>
          </div>
        </div>
        <button class="text-blue-500 font-bold">Follow</button>
      </div>
    </div>
  </template>
  
  <script>
  import suggestedUsersData from '/db.json'; // Importer les données JSON
  
  export default {
    name: "FollowPerson",
    data() {
      return {
        suggestedUsers: suggestedUsersData.suggestedUsers
      };
    }
  };
  </script>
  
  <style scoped>
  /* Ajoutez vos styles ici */
  </style>
  