<script setup>

import {computed} from "vue";

const props = defineProps({
  iconImage: String,
})

const imageUrl = computed(() => {
  return new URL(`../assets/img/${props.iconImage}`, import.meta.url).href;
});

</script>

<template>

  <div class="md:w-[250px] w-[300px] p-6 h-auto services-item bg-teal-100 rounded-xl m-[20px]">
    <span><slot name="service-icon"><img class="w-10" :src="imageUrl" alt=""></slot></span>
      <h2 class="text-2 my-2 font-bold"><slot name="service-title"></slot></h2>
      <p><slot name="service-text"></slot></p>
  </div>

</template>

<style scoped>

</style>