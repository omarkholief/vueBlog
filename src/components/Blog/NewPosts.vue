<script setup>
import { onMounted, ref } from 'vue'
import axios from 'axios'
import SinglePost from './SinglePost.vue'

const posts = ref([])
const getPosts = async () => {
  try {
    const res = await axios(
      'https://newsapi.org/v2/top-headlines?sources=techcrunch&apiKey=80187c7925854a9ea1b66640fb1cbc78'
    )
    posts.value = res.data.articles
  } catch (error) {
    console.error(error)
  }
}
onMounted(async () => await getPosts())
</script>
<template>
  <div class="py-8">
    <div class="my-4 flex gap-4 items-center py-8 justify-center">
      <label for="search">Search Post</label>
      <input
        type="text"
        placeholder="search post"
        class="ring ring-gray-200 px-4 py-2 w-full lg:w-96 outline-none rounded-lg" />
    </div>
    <ul class="grid grid-cols-1 lg:grid-cols-3 gap-8">
      <SinglePost
        v-for="post in posts"
        :post="post" />
    </ul>
  </div>
</template>

<style></style>
