<script setup>
import { onMounted, ref, computed } from 'vue'
import axios from 'axios'
import SinglePost from './SinglePost.vue'

const search = ref('')
const posts = ref([])
const loading = ref(false)
const apiKey = 'd483bf05-6c39-44dc-8f0c-fe371b606909'
const getPosts = async () => {
  loading.value = true
  try {
    const res = await axios(
      `https://eventregistry.org/api/v1/article/getArticles?apiKey=${apiKey}&action=getArticles&keyword=Tesla Inc&lang=eng`
    )
    console.log(res)
    posts.value = res.data.articles.results

    loading.value = false
  } catch (error) {
    console.error(error)
  }
}
onMounted(async () => await getPosts())

const filterPosts = computed(() => {
  return posts.value.filter((post) => {
    return post.title.toLowerCase().includes(search.value.toLowerCase().trim())
  })
})
</script>
<template>
  <div>
    <div
      v-if="loading"
      class="h-96 flex items-center justify-center">
      <div role="status">
        <svg
          aria-hidden="true"
          class="w-16 h-16 text-gray-200 animate-spin dark:text-gray-600 fill-blue-600"
          viewBox="0 0 100 101"
          fill="none"
          xmlns="http://www.w3.org/2000/svg">
          <path
            d="M100 50.5908C100 78.2051 77.6142 100.591 50 100.591C22.3858 100.591 0 78.2051 0 50.5908C0 22.9766 22.3858 0.59082 50 0.59082C77.6142 0.59082 100 22.9766 100 50.5908ZM9.08144 50.5908C9.08144 73.1895 27.4013 91.5094 50 91.5094C72.5987 91.5094 90.9186 73.1895 90.9186 50.5908C90.9186 27.9921 72.5987 9.67226 50 9.67226C27.4013 9.67226 9.08144 27.9921 9.08144 50.5908Z"
            fill="currentColor" />
          <path
            d="M93.9676 39.0409C96.393 38.4038 97.8624 35.9116 97.0079 33.5539C95.2932 28.8227 92.871 24.3692 89.8167 20.348C85.8452 15.1192 80.8826 10.7238 75.2124 7.41289C69.5422 4.10194 63.2754 1.94025 56.7698 1.05124C51.7666 0.367541 46.6976 0.446843 41.7345 1.27873C39.2613 1.69328 37.813 4.19778 38.4501 6.62326C39.0873 9.04874 41.5694 10.4717 44.0505 10.1071C47.8511 9.54855 51.7191 9.52689 55.5402 10.0491C60.8642 10.7766 65.9928 12.5457 70.6331 15.2552C75.2735 17.9648 79.3347 21.5619 82.5849 25.841C84.9175 28.9121 86.7997 32.2913 88.1811 35.8758C89.083 38.2158 91.5421 39.6781 93.9676 39.0409Z"
            fill="currentFill" />
        </svg>
        <span class="sr-only">Loading...</span>
      </div>
    </div>
    <div
      v-else
      class="py-8">
      <div class="my-4 flex gap-4 items-center py-8 justify-center">
        <label for="search">Search Post</label>
        <input
          v-model="search"
          type="text"
          placeholder="search post"
          class="ring ring-gray-200 px-4 py-2 w-full lg:w-96 outline-none rounded-lg" />
      </div>
      <ul class="grid grid-cols-1 lg:grid-cols-3 gap-8">
        <SinglePost
          v-for="post in filterPosts"
          :post="post" />
      </ul>
    </div>
  </div>
</template>

<style></style>
