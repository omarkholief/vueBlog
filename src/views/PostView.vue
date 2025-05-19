<script setup>
import { onMounted, ref } from 'vue'
import { useRoute, useRouter } from 'vue-router'
import axios from 'axios'
const apiKey = 'YOUR_API_KEY'
const post = ref(null)
const route = useRoute()

// const getPost = async () => {
//   try {
//     const res = await axios(
//       `https://eventregistry.org/api/v1/article/getArticle?apiKey=${apiKey}&action=getArticle&articleUri=${route.params.postId}`
//     )
//     post.value = res.data
//   } catch (error) {
//     console.error(error)
//   }
// }


const getPost = async () => {
  try {
    console.log("API KEY:", apiKey)
    console.log("Post ID:", route.params.postId)

    const res = await axios(
      `https://eventregistry.org/api/v1/article/getArticle?${apiKey}&action=getArticle&articleUri=${route.params.postId}`
    )
    post.value = res.data
  } catch (error) {
    console.error("Axios Error:", error.response?.data || error.message)
  }
}




onMounted(async () => {
  const id = route.params.postId        // هتلاقيها postId مش undefined
  console.log('param:', id)
  post.value = await getPost(id)       // أو أي دالة عندك
})

onMounted(async () => await getPost())
</script>
<template>
  <div v-if="post">
    <h1 class="text-2xl font-bold mb-4">{{ post.title }}</h1>
    <p class="text-sm text-gray-500 mb-6">Published: {{ post.publishedAt }}</p>
    <div v-html="post.content" class="mb-6"></div>
  </div>
  <div v-else>Loading...</div>
</template>

<style lang="scss"></style>
