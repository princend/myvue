<template>
  <div class="post-list">
    <h2>Recent Posts</h2>
    <ul>
      <li v-for="post in posts" :key="post.id" class="post-item">
        <h3>{{ post.title }}</h3>
        <p>{{ post.snippet }}</p>
        <a href="#">Read More &rarr;</a>
      </li>
    </ul>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue';

const posts = ref([
  { id: 1, title: 'Why Otters Hold Hands', snippet: 'Discover the adorable reason why sea otters often float hand-in-hand...' },
  { id: 2, title: 'A Guide to Different Otter Species', snippet: 'From the giant river otter to the smal-clawed otter, learn about the diversity...' },
  { id: 3, title: 'Otter Pups: Cuteness Overload!', snippet: 'Everything you need to know about baby otters, known as pups or kittens...' },
]);
</script>

<style scoped>
.post-list {
  max-width: 800px;
  margin: 20px auto;
  padding: 0 15px;
}

.post-list h2 {
    color: #8B4513; /* Saddle Brown */
    border-bottom: 2px solid #ADD8E6; /* Light Blue */
    padding-bottom: 5px;
    margin-bottom: 20px;
}

.post-item {
  background-color: #F0F8FF; /* Alice Blue - Light watery feel */
  border: 1px solid #ADD8E6; /* Light Blue */
  padding: 15px;
  margin-bottom: 15px;
  border-radius: 5px;
  list-style-type: none; /* Remove default bullet points */
}

.post-item h3 {
  margin-top: 0;
  color: #0056b3; /* Darker Blue for title */
}

.post-item a {
    color: #5F9EA0; /* Cadet Blue */
    text-decoration: none;
    font-weight: bold;
}
.post-item a:hover {
    text-decoration: underline;
}
</style>