<script setup>
import { ref } from 'vue';

// Dynamically load background image
const bgImage = ref(new URL('@/assets/img/cleaning.jpg', import.meta.url).href);
</script>

<template>
  <div
      class="h-[calc(100vh-100px)] mt-[90px] flex items-center bg-blue-100 relative z-1 showcase-wrapper"
      :style="{ backgroundImage: `linear-gradient(rgba(0,0,0,0.5),rgba(0,0,0,0.5)), url(${bgImage})` }">
    <div class="text-white md:ml-30 h-auto px-6 md:px-20 text-center md:text-left">
      <h1 class="text-4xl md:text-7xl mb-5 font-bold">MM HomeCleaning</h1>
      <p class="text-lg md:text-2xl">Reliable, Efficient, and Affordable Home Cleaning Services. Let Us Make Your Home Shine!</p>
      <a href="tel:9259893623" class="mt-5 inline-block bg-lime-300 text-black py-2 px-6 md:px-10 rounded-3xl transition duration-200 hover:bg-lime-400">
        Call now
      </a>
    </div>
  </div>
</template>

<style scoped>
.showcase-wrapper {
  background-image: linear-gradient(rgba(0,0,0,0.5),rgba(0,0,0,0.5)), url('@/assets/img/cleaning.jpg');
  background-size: cover;
  background-position: center;
}
</style>