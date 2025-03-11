<script setup>

</script>

<template>

  <div class="hero-text contact p-10 md:flex md:items-center md:justify-center">
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

@keyframes heroText {
  0% {
    opacity: 0;
    transform: translateY(100px);
  }
  100% {
    opacity: 1;
    transform: translateY(0);
  }
}

.hero-text {
  animation: heroText 1.5s ease-out forwards;
}

</style>