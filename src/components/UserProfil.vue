<template>
    <img :src="profile_image" alt="Profile Image" class="h-8 w-8 rounded-full">
  </template>
  
  <script>
  export default {
    props: {
      profile_image: String
    }
  };
  </script>
  
  <style>
  /* Ajoutez vos styles ici */
  </style>
  