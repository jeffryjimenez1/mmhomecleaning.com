<script setup>
import ServicesItem from "@/components/ServicesItem.vue";

</script>

<template>
    <div class="services hero-text">
      <div class="heroText services-title w-full text-center mt-10 md:text-6xl text-3xl">
        OUR SERVICES
      </div>

      <div class="services-content flex flex-wrap justify-center md:p-10 md:w-[60%] m-auto">
        <ServicesItem icon-image="room.png">
          <template #service-title>Room Cleaning</template>
          <template #service-text>We tidy up your room, dust, vacuum, and make your space fresh and inviting.</template>
        </ServicesItem>

        <ServicesItem icon-image="kitchen.png">
          <template #service-title>Kitchen Cleaning</template>
          <template #service-text>We scrub countertops, clean appliances, and sanitize surfaces for a spotless kitchen.</template>
        </ServicesItem>

        <ServicesItem icon-image="bathroom.png">
          <template #service-title>Bathroom Cleaning</template>
          <template #service-text>Deep cleaning for sinks, toilets, tubs, and mirrors to ensure a sparkling bathroom.</template>
        </ServicesItem>

        <ServicesItem icon-image="garage.png">
          <template #service-title>Garage Cleaning</template>
          <template #service-text>We declutter, sweep, and organize your garage to maximize space and cleanliness.</template>
        </ServicesItem>

        <ServicesItem icon-image="living.png">
          <template #service-title>Living Room Cleaning</template>
          <template #service-text>Dusting, vacuuming, and furniture cleaning to keep your living space fresh and welcoming.</template>
        </ServicesItem>

        <ServicesItem icon-image="dishes.png">
          <template #service-title>Dishes Cleaning</template>
          <template #service-text>We wash, dry, and organize your dishes so you can enjoy a spotless kitchen effortlessly.</template>
        </ServicesItem>
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