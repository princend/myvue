<template>
  <div id="app">
    <Header />
    <main>
      <PostList />
      <!-- We will add Vue Router here later to show different pages -->
    </main>
    <Footer />
  </div>
</template>

<script setup lang="ts">
import Header from './components/Header.vue';
import Footer from './components/Footer.vue';
import PostList from './components/PostList.vue';
// HelloWorld component is no longer used directly here
// import HelloWorld from './components/HelloWorld.vue'
</script>

<style scoped>
/* Styles for the main app container can go here if needed */
/* For example, ensuring footer stays at the bottom if content is short */
#app {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
}

main {
  flex: 1; /* Allows the main content area to grow and push the footer down */
}
</style>