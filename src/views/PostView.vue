<script setup>
import { onMounted, ref } from 'vue'
import { useRoute, useRouter } from 'vue-router'
import axios from 'axios'
const apiKey = ''
const post = ref(null)
const route = useRoute()

const getPost = async () => {
  try {
    const res = await axios(
      `https://eventregistry.org/api/v1/article/getArticle?apiKey=${apiKey}&action=getArticle&articleUri=${route.params.postId}`
    )
    post.value = res.data
  } catch (error) {
    console.error(error)
  }
}
onMounted(async () => await getPost())
</script>
<template>
  <div class="container mx-auto max-w-7xl min-h-screen px-8">
    {{ $route.params.postId }}
    <div>
      {{ post }}
    </div>
  </div>
</template>

<style lang="scss"></style>
