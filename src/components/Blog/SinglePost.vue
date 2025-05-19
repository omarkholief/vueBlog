<script setup>
import { computed } from 'vue'
import { format } from 'date-fns'

const props = defineProps(['post'])
const post = computed(() => props.post)
</script>
<template>
  <li class="ring ring-gray-200 shadow-sm rounded-xl overflow-hidden">
    <div class="w-full h-64 overflow-hidden">
      <img :src="post.image ? post.image : 'https://placehold.co/600x400/EEE/31343C'" :alt="post.title + 'image'"
        class="w-full h-full object-cover" />
    </div>
    <div class="p-4">

      <RouterLink :to="{ name: 'post', params: { postId: post.uri } }">
        <h1 class="font-bold text-lg my-2 line-clamp-2">{{ post.title }}</h1>
      </RouterLink>

      <!-- <RouterLink :to="'/posts/' + post.uri">
        <h1 class="font-bold text-lg my-2 line-clamp-2">{{ post.title }}</h1>
      </RouterLink> -->
      <p class="text-sm mb-2">published At: {{ post.date }}</p>
      <p class="text-gray-500 line-clamp-2 mb-4">
        {{ post.body }}
      </p>
      <p v-if="post.authors.length">Author: {{ post.authors[0].name }}</p>
    </div>
  </li>
</template>

<style></style>
