<template>
    <div class="flex justify-center items-center w-full">
      <div class="flex items-center gap-20">
        <div class="flex-1 text-center">
          <a href="#" class="w-12 mt-1 group flex items-center text-gray-500 px-3 py-2 text-base leading-6 font-medium rounded-full hover:bg-blue-400 hover:text-blue-300">
            <svg class="text-center h-6 w-6" fill="none" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" stroke="currentColor" viewBox="0 0 24 24">
              <path d="M8 12h.01M12 12h.01M16 12h.01M21 12c0 4.418-4.03 8-9 8a9.863 9.863 0 01-4.255-.949L3 20l1.395-3.72C3.512 15.042 3 13.574 3 12c0-4.418 4.03-8 9-8s9 3.582 9 8z"></path>
            </svg>
          </a>
        </div>
  
        <div class="flex-1 text-center py-2 m-2">
          <a href="#" class="w-12 mt-1 group flex items-center text-gray-500 px-3 py-2 text-base leading-6 font-medium rounded-full hover:bg-blue-400 hover:text-blue-300">
            <svg class="text-center h-7 w-6" fill="none" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" stroke="currentColor" viewBox="0 0 24 24">
              <path d="M7 16V4m0 0L3 8m4-4l4 4m6 0v12m0 0l4-4m-4 4l-4-4"></path>
            </svg>
          </a>
        </div>
  
        <div class="flex-1 text-center py-2 m-2">
          <a href="#" @click="toggleHeart" class="w-12 mt-1 group flex items-center text-gray-500 px-3 py-2 text-base leading-6 font-medium rounded-full hover:bg-blue-400 hover:text-blue-300">
            <svg class="text-center h-7 w-6" fill="none" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" :class="{'text-red-500': isHeartRed, 'text-gray-500': !isHeartRed}" stroke="currentColor" viewBox="0 0 24 24">
              <path :class="{'fill-current': isHeartRed, 'fill-none': !isHeartRed}" d="M4.318 6.318a4.5 4.5 0 000 6.364L12 20.364l7.682-7.682a4.5 4.5 0 00-6.364-6.364L12 7.636l-1.318-1.318a4.5 4.5 0 00-6.364 0z"></path>
            </svg>
          </a>
        </div>
  
        <div class="flex-1 text-center py-2 m-2">
          <a href="#" class="w-12 mt-1 group flex items-center text-gray-500 px-3 py-2 text-base leading-6 font-medium rounded-full hover:bg-blue-400 hover:text-blue-300">
            <svg class="text-center h-7 w-6" fill="none" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" stroke="currentColor" viewBox="0 0 24 24">
              <path d="M4 16v1a3 3 0 003 3h10a3 3 0 003-3v-1m-4-8l-4-4m0 0L8 8m4-4v12"></path>
            </svg>
          </a>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    name: "IconsTweets",
    data() {
      return {
        isHeartRed: false,
      };
    },
    methods: {
      toggleHeart() {
        this.isHeartRed = !this.isHeartRed;
      },
    },
  };
  </script>
  
  <style>
  .fill-current {
    fill: currentColor;
  }
  .fill-none {
    fill: none;
  }
  </style>
  