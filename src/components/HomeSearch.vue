<template>
    <div class="flex-1 px-2 pt-2  mb-4">
        <input
          type="text"
          class="bg-gray-200 rounded-full border text-gray-400 h-10 font-medium text-lg w-full pl-4"
          placeholder="What's happening?"
          v-model="newTweetContent"
          @keydown.enter.prevent="addTweet"
        />
 </div>
    <div class="flex items-center">
        <button
        class="bg-blue-400 w-28  hover:bg-blue-600 text-white font-bold rounded-full"
        @click="addTweet"
      >
        Add Tweet
      </button>
                      
    </div>

</template>
<script>
export default {
    name : "HomeSearch",
}
</script>
<style>
</style>