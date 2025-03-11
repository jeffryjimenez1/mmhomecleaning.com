<script setup>
import { ref, onMounted } from "vue";
import Showcase from "@/components/Showcase.vue";
import Services from "@/components/Services.vue";
import About from "@/components/About.vue";
import Contact from "@/components/Contact.vue";
import Footer from "@/components/Footer.vue";

// Track visibility for each section
const isServicesVisible = ref(false);
const isAboutVisible = ref(false);
const isContactVisible = ref(false);

const observeElement = (target, callback) => {
  const observer = new IntersectionObserver(
      (entries) => {
        if (entries[0].isIntersecting) {
          callback(true);
          observer.disconnect(); // Stop observing after it's loaded
        }
      },
      { threshold: 0.1 } // Adjust to control when it loads (0.1 = 10% visible)
  );

  if (target) observer.observe(target);
};

onMounted(() => {
  observeElement(document.getElementById("services-section"), (val) => (isServicesVisible.value = val));
  observeElement(document.getElementById("about-section"), (val) => (isAboutVisible.value = val));
  observeElement(document.getElementById("contact-section"), (val) => (isContactVisible.value = val));
});
</script>

<template>
  <main>
    <Showcase />

    <!-- Lazy load Services -->
    <div id="services-section">
      <Services v-if="isServicesVisible" />
    </div>

    <!-- Lazy load About -->
    <div id="about-section">
      <About v-if="isAboutVisible" />
    </div>

    <!-- Lazy load Contact -->
    <div id="contact-section">
      <Contact v-if="isContactVisible" />
    </div>

    <Footer />
  </main>
</template>
