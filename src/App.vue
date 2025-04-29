<script setup>
// scrollToTop Function
const scrollToTop = () => {
  window.scrollTo({ top: 0, behavior: 'smooth' });
};

</script>

<template>
  <!-- Create Header -->
  <header class="sticky top-0 z-50 bg-white shadow container item-center py-2">
    <nav class="flex justify-between mx-auto max-w-7xl py-4 px-6 rounded-xl">
      <a href="/" class="text-2xl font-semibold">Blogloo</a>
      <div class="flex gap-2 items-center">
        <p class="cursor-pointer">Light</p>
        <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none"
          stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" data-lucide="moon"
          class="lucide lucide-moon top-icon w-5 h-5 light cursor-pointer">
          <path d="M12 3a6 6 0 0 0 9 9 9 9 0 1 1-9-9Z"></path>
        </svg>
        <p class="cursor-pointer">Dark</p>
      </div>
    </nav>
  </header>
  <!-- Create Section -->
  <section class="max-w-7xl container item-center text-center my-20 mx-auto">
    <h1 class="text-5xl font-bold">Blogs Section For Everyone</h1>
    <p class="max-w-md mx-auto my-5 text-gray-500 dark:text-gray-400 text-lg text-center font-medium">Lorem Ipsum is
      simply dummy text of the printing
      and typesetting industry.</p>
  </section>
  <!-- Create Section Cards -->
  <section class="max-w-7xl container item-center mx-auto">
    <ul
      class="grid grid-cols-12 sm:grid-cols-12 md:grid-cols-12 lg:grid-cols-12 xl:grid-cols-12 gap-4 mb-4 items-center">
      <li class="col-span-12 sm:col-span-12  md:col-span-6 lg:col-span-4 xl:col-span-4">
        <div><a href="#"><img class="rounded-t-lg" src="./assets/images/s-2.jpg" alt=""></a></div>
        <div
          class="bg-white backdrop-blur-2xl rounded-md w-full relative transform translate-y-0 hover:-translate-y-4 duration-500 ease-in-out mb-8 sm:mb-8 lg:mb-0">
          <div class="flex-auto text-center p-8 md:p-14 pb-5 md:pb-5">
            <img
              class="inline-flex absolute top-0 left-[50%] start-[50%] -translate-x-[50%] -translate-y-[50%] justify-center items-center h-[80px] w-[80px] rounded-full bg-primary-50  dark:bg-gray-800/40 backdrop-blur-2xl border-[5px] border-solid border-white"
              src="./assets/images/avatar-2.jpg" alt="">
            <h1 class="my-3 block text-[20px] font-medium tracking-tight text-gray-900">Popular admin
              template you can use for your business.</h1>
            <div class="block mt-5">
              <a href="#">
                <button
                  class=" cursor-pointer transition-all text-blue-500 bg-gray-100 hover:text-white text-primary-500 hover:bg-blue-500 bg-primary-500/5 text-base font-medium py-[6px] px-5 rounded-full print:hidden">
                  Read More
                </button>
              </a>
            </div>
          </div>
          <!-- End Card -->
          <div class="flex-auto">
            <div class="px-3 bg-primary-500/5 text-primary-500 pt-3 pb-1">
              <marquee class="w-full text-blue-500 border-t" direction="left">
                Contrary to popular belief, Lorem Ipsum is not simply random text.
              </marquee>
            </div>
          </div>
        </div>
      </li>
      <li class="col-span-12 sm:col-span-12  md:col-span-6 lg:col-span-4 xl:col-span-4">
        <div><a href="#"><img class="rounded-t-lg" src="./assets/images/s-1.jpg" alt=""></a></div>
        <div
          class="bg-white backdrop-blur-2xl rounded-md w-full relative transform translate-y-0 hover:-translate-y-4 duration-500 ease-in-out mb-8 sm:mb-8 lg:mb-0">
          <div class="flex-auto text-center p-8 md:p-14 pb-5 md:pb-5">
            <img
              class="inline-flex absolute top-0 left-[50%] start-[50%] -translate-x-[50%] -translate-y-[50%] justify-center items-center h-[80px] w-[80px] rounded-full bg-primary-50  dark:bg-gray-800/40 backdrop-blur-2xl border-[5px] border-solid border-white"
              src="./assets/images/avatar-4.jpg" alt="">
            <h1 class="my-3 block text-[20px] font-medium tracking-tight text-gray-90">Popular admin
              template you can use for your business.</h1>
            <div class="block mt-5">
              <a href="#">
                <button
                  class=" text-blue-500 bg-gray-100 cursor-pointer transition-all hover:text-white text-primary-500 hover:bg-blue-500 bg-primary-500/5 text-base font-medium py-[6px] px-5 rounded-full print:hidden">
                  Read More
                </button>
              </a>
            </div>
          </div>
          <!-- End Card -->
          <div class="flex-auto">
            <div class="px-3 bg-primary-500/5 text-primary-500 pt-3 pb-1">
              <marquee class="w-full text-blue-500 border-t" direction="left">
                Contrary to popular belief, Lorem Ipsum is not simply random text.
              </marquee>
            </div>
          </div>
        </div>
      </li>
      <li class="col-span-12 sm:col-span-12  md:col-span-6 lg:col-span-4 xl:col-span-4">
        <div><a href="#"><img class="rounded-t-lg" src="./assets/images/s-3.jpg" alt=""></a></div>
        <div
          class="bg-white backdrop-blur-2xl rounded-md w-full relative transform translate-y-0 hover:-translate-y-4 duration-500 ease-in-out mb-8 sm:mb-8 lg:mb-0">
          <div class="flex-auto text-center p-8 md:p-14 pb-5 md:pb-5">
            <img
              class="inline-flex absolute top-0 left-[50%] start-[50%] -translate-x-[50%] -translate-y-[50%] justify-center items-center h-[80px] w-[80px] rounded-full bg-primary-50  dark:bg-gray-800/40 backdrop-blur-2xl border-[5px] border-solid border-white"
              src="./assets/images/avatar-5.jpg" alt="">
            <h1 class="my-3 block text-[20px] font-medium tracking-tight text-gray-900">Popular admin
              template you can use for your business.</h1>
            <div class="block mt-5">
              <a href="#">
                <button
                  class=" text-blue-500 bg-gray-100 cursor-pointer hover:text-white text-primary-500 hover:bg-blue-500 transition-all bg-primary-500/5 text-base font-medium py-[6px] px-5 rounded-full print:hidden">
                  Read More
                </button>
              </a>
            </div>
          </div>
          <!-- End Card -->
          <div class="flex-auto">
            <div class="px-3 bg-primary-500/5 text-primary-500 pt-3 pb-1">
              <marquee class="w-full text-blue-500 border-t" direction="left">
                Contrary to popular belief, Lorem Ipsum is not simply random text.
              </marquee>
            </div>
          </div>
        </div>
      </li>
    </ul>
  </section>
  <!-- Create Button Smoothies -->
  <button @click="scrollToTop"
    class=" cursor-pointer fixed bottom-6 right-6 bg-blue-600 text-white px-4 py-2 rounded-full shadow-lg hover:bg-blue-700 transition">
    ↑ Top
  </button>
</template>

<style scoped></style>