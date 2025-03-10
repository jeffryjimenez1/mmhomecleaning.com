<script setup>
import Footer from "@/components/Footer.vue";
</script>

<template>
  <div class="md:h-[calc(100vh-50px)] mt-12 bg-green-100 mission md:flex md:flex-col md:align-center md:justify-center p-10 mt-[90px]">

    <div class="bg-teal-100 md:w-1/2 m-auto about-text p-5 rounded-lg">
      <h1 class="md:text-5xl text-2xl text-center">Our Mission</h1>
      <p class="md:text-2xl text-1xl mt-5 leading-relaxed">At MM Homecleaning, our mission is to create cleaner, healthier, and more comfortable spaces for our clients. We are committed to delivering high-quality cleaning services with professionalism, reliability, and attention to detail. Our team takes pride in using eco-friendly products and industry-leading techniques to ensure every home and business we serve is spotless, safe, and inviting.

        We believe that a clean environment enhances well-being, productivity, and peace of mind. That’s why we go above and beyond to exceed expectations—because your satisfaction is our priority. Whether it’s residential, commercial, or specialized cleaning, we’re here to make cleanliness effortless for you.

        Let us do the cleaning, so you can focus on what truly matters!</p>
    </div>

  </div>
  <Footer/>
</template>

<style scoped>

.mission   {
  background-image: url('@/assets/img/cleaning2.jpg');
  background-size: cover;
  background-position: center;
}

@media (min-width: 1024px) {

}
</style>
