<script setup>
import {onBeforeUnmount, onMounted, ref} from "vue";

const sectionRef = ref(null);
const isVisible = ref(false);
let observer = null;

onMounted(()=> {
  observer = new IntersectionObserver((entries)=>{
    entries.forEach((entry) => {
      if (entry.isIntersecting) {
        isVisible.value = true;
      }
    })
  },{ threshold: 0.1 })

  if(sectionRef.value) {
    observer.observe(sectionRef.value);
  }
});

onBeforeUnmount(() => {
  if (observer && sectionRef.value) {
    observer.unobserve(sectionRef.value);
  }
});
</script>

<template>

  <div ref="sectionRef" class="contact p-10 md:flex md:items-center md:justify-center"
       :class="{ visible: isVisible, 'contact-text-section': isVisible }"
  >
    <div class="contact-pic md:w-1/3 md:order-1 mt-[90px]">
      <img src="../assets/img/contact.jpg" alt="" class="h-[400px]">
    </div>
    <div class="md:w-[40%] contact-text text-left">

      <h2 class="md:text-5xl text-4xl mt-10">Contact Us</h2>

      <p class="my-8 md:text-2xl">Tel: <a class="hover:text-sky-700" href="tel:+9259893623">925-989-3623</a></p>
      <p class="my-8 md:text-2xl">Email: <a class="hover:text-sky-700" href="mailto:vanessa@thespecific.com">vanessa@thespecific.com</a> </p>

    </div>
  </div>

</template>

<style scoped>

@keyframes contactText {
  0% {
    opacity: 0;
    transform: translateY(200px);
  }
  100% {
    opacity: 1;
    transform: translateY(0);
  }
}

.contact-text-section {
  opacity: 0;
  animation: contactText 1.5s ease-out forwards;
}


.contact-text-section.visible {
  opacity: 1;
}


</style>