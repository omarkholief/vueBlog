<script setup>
import { RouterLink, RouterView } from 'vue-router'
import TheHeader from './components/TheHeader.vue'
// scrollToTop Function
const scrollToTop = () => {
  window.scrollTo({ top: 0, behavior: 'smooth' })
}
</script>

<template>
  <!-- Create Header -->
  <TheHeader />

  <RouterView />
</template>

<style scoped></style>
