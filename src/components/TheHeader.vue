<template>
  <header class="sticky top-0 z-50 bg-white shadow item-center py-2 w-full mx-auto">
    <nav class="flex justify-between mx-auto max-w-7xl py-4 px-6 rounded-xl">
      <div class="flex gap-4 items-center">
        <RouterLink to="/">Home</RouterLink>
        <RouterLink to="/about">About</RouterLink>
      </div>

      <div class="flex gap-2 items-center">
        <p class="cursor-pointer">Light</p>
        <svg
          xmlns="http://www.w3.org/2000/svg"
          width="24"
          height="24"
          viewBox="0 0 24 24"
          fill="none"
          stroke="currentColor"
          stroke-width="2"
          stroke-linecap="round"
          stroke-linejoin="round"
          data-lucide="moon"
          class="lucide lucide-moon top-icon w-5 h-5 light cursor-pointer">
          <path d="M12 3a6 6 0 0 0 9 9 9 9 0 1 1-9-9Z"></path>
        </svg>
        <p class="cursor-pointer">Dark</p>
      </div>
    </nav>
  </header>
</template>

<script lang="ts" setup></script>

<style></style>
