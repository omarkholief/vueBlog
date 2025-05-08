<script setup>
import { ref } from 'vue'
import { format } from 'date-fns'

const props = defineProps(['post'])
const post = ref(props.post)

// const formateDate = () => {
//   return format(new Date(post.value.publishedAt), 'dd MMMM-yyy')
// }
</script>
<template>
  <li class="ring ring-gray-200 shadow-sm rounded-xl overflow-hidden">
    <div class="w-full h-64 overflow-hidden">
      <img
        :src="post.urlToImage"
        :alt="post.title + 'image'"
        class="w-full h-full object-cover" />
    </div>
    <div class="p-4">
      <h1 class="font-bold text-lg my-2 line-clamp-2">{{ post.title }}</h1>
      <p class="text-sm mb-2">
        published At: {{ format(new Date(post.publishedAt), 'dd MMM-yyy') }}
      </p>
      <p class="text-gray-500 line-clamp-2 mb-4">
        {{ post.content }}
      </p>
      <p>Author: {{ post.author }}</p>
    </div>
  </li>
</template>

<style></style>
