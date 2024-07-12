<template>
  <body class=" h-screen">
    <div class="flex">

      <div class="h-12 pl-9 py-4 h-auto">
        <!-- Barre de navigation -->
        <AppNavbar />
      </div>
        <!-- Contenu principal -->
        <main class="container mx-auto flex">
          <!-- Timeline des tweets -->
          <section class="w-4/6 p-4">
            <TweetTimeline />
          </section>

          <!-- Suggestions d'utilisateurs -->
          <aside class="w-1/3 p-4">
            <UserSuggestions />
          </aside>
        </main>
      
    </div>
  </body>
</template>

<script>
import AppNavbar from './components/AppNavbar.vue';
import TweetTimeline from './components/TweetTimeline.vue';
import UserSuggestions from './components/UserSuggestions.vue';

export default {
  name : "App",
  components: {
    AppNavbar,
    TweetTimeline,
    UserSuggestions
  }
}
</script>

<style>
/* Styles globaux ou spécifiques à App.vue */
</style>
