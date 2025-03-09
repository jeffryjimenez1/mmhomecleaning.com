<script setup>
import { ref } from "vue";
import { useLoadScript } from "@fawmi/vue-google-maps";

// Load the Google Maps script
useLoadScript({
  key: "YOUR_GOOGLE_MAPS_API_KEY", // Replace with your actual API key
});

const center = ref({ lat: 37.7749, lng: -122.4194 });
</script>

<template>
  <GMapMap
      :center="center"
      :zoom="12"
      style="width: 100%; height: 500px"
  >
    <GMapMarker
        :position="center"
        :clickable="true"
        :draggable="false"
    />
  </GMapMap>
</template>
