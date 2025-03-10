<script setup>
import { RouterLink, RouterView } from 'vue-router'
import { ref, computed, onMounted } from 'vue';
import { useRoute } from 'vue-router';

const route = useRoute();
const isMenuOpen = ref(false);

const links = [
  { name: "Home", path: "/" },
  { name: "Our Mission", path: "/mission" },
  { name: "Contact", path: "/contact" }
];

const isActive = (path) => computed(() => route.path === path);

const toggleMenu = () => {
  isMenuOpen.value = !isMenuOpen.value;
};
</script>

<template>
  <nav class="bg-white w-full fixed top-0 z-50 px-6 md:px-[200px] py-4 flex items-center justify-between shadow-md">
    <router-link to="/" class="logo">
      <img class="w-12 md:w-16 rounded-full" src="../assets/img/logo.jpg" alt="Logo">
    </router-link>

    <button @click="toggleMenu" class="md:hidden text-black focus:outline-none">
      <svg v-if="!isMenuOpen" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor" class="w-8 h-8">
        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16m-7 6h7"></path>
      </svg>
      <svg v-else xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor" class="w-8 h-8">
        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12"></path>
      </svg>
    </button>

    <div class="hidden md:flex space-x-6">
      <router-link
          v-for="link in links"
          :key="link.path"
          :to="link.path"
          class="px-4 py-2 rounded transition duration-200 ease-in"
          :class="isActive(link.path).value ? 'bg-lime-300 text-black rounded-full' : 'text-black hover:bg-lime-300 rounded-full'">
        {{ link.name }}
      </router-link>
    </div>

    <div v-if="isMenuOpen" class="absolute top-16 left-0 w-full bg-white md:hidden flex flex-col items-center shadow-md">
      <router-link
          v-for="link in links"
          :key="link.path"
          :to="link.path"
          class="w-full text-center py-3 border-b"
          :class="isActive(link.path).value ? 'bg-lime-300 text-black' : 'text-black hover:bg-lime-300'">
        {{ link.name }}
      </router-link>
    </div>
  </nav>

  <RouterView />
</template>
