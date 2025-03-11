<script setup>

</script>

<template>
    <div class="hero-text bg-teal-100 about md:h-screen md:flex md:items-center py-10">
      <div class="about-pic m-auto md:ml-0 md:w-1/2 md:h-[90%] h-[300px] w-[80%]"></div>

      <div class="about-text md:w-[60%] p-10">
        <h2 class="md:text-4xl md:mb-4 text-3xl">
          Trusted Cleaning Services in California for Over 10 Years
        </h2>
        <p class="text-1xl leading-loose md:w-[80%]">
          For over a decade, MM HomeCleaning has been the go-to cleaning service for homes and businesses across California.
          Our commitment to excellence, reliability, and customer satisfaction has earned us a reputation as a trusted leader in the cleaning industry.
        </p>
        <p>
          With over 10 years of experience, we understand that a clean home is more than just a necessity—it’s a reflection of comfort, health, and well-being.
          Our team of skilled professionals is dedicated to providing top-tier cleaning solutions tailored to your specific needs.
        </p>
        <p class="mt-4">
          We specialize in:
          <span class="block"></span>
          ✔ <strong>Residential Cleaning</strong> – From routine housekeeping to deep cleaning, we keep your home fresh and spotless.<br />
          ✔ <strong>Kitchen & Bathroom Cleaning</strong> – Thorough sanitization of high-use areas for a healthier living space.<br />
          ✔ <strong>Move-In & Move-Out Cleaning</strong> – Ensuring your new home is clean and move-in ready.<br />
          ✔ <strong>Eco-Friendly Cleaning</strong> – Using safe, non-toxic products for a healthier environment.<br /><br />
        </p>
        <p>
          At MM HomeCleaning, we pride ourselves on punctuality, professionalism, and attention to detail. Whether you need a one-time deep clean or regular maintenance, our team is ready to exceed your expectations.
          <span class="block"></span>
          📍 Proudly serving California for 10+ years!<br />
          📞 Contact us today and let us make your home shine! ✨
        </p>
        <a href="tel:9259893623" class="mt-5 inline-block bg-lime-300 text-black py-2 px-6 md:px-10 rounded-3xl transition duration-200 hover:bg-lime-400">
          Call now
        </a>
      </div>
    </div>
</template>

<style scoped>
.about-pic {
  background-image: url('@/assets/img/about.jpg');
  background-size: cover;
  background-position: center;
}


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
