<script setup>
import { RouterLink, RouterView } from 'vue-router'
import TheHeader from './components/TheHeader.vue'
// scrollToTop Function
const scrollToTop = () => {
  window.scrollTo({ top: 0, behavior: 'smooth' })
}
</script>

<template>
  <div>
    <!-- Create Header -->
    <TheHeader />

    <RouterView />
  </div>
</template>

<style scoped></style>
