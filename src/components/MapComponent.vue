<template>
  <GoogleMap
    :api-key="apiKey"
    :mapId="mapId"
    style="width: 100%; height: 500px"
    :center="center"
    :zoom="15"
  >
    <AdvancedMarker :options="{ position: center }" />
  </GoogleMap>
</template>

<script lang="ts" setup>
import { GoogleMap, AdvancedMarker } from "vue3-google-map";

const center = { lat: 46.94849280588769, lng: 7.44748922864467 };

const apiKey = import.meta.env.VITE_GOOGLE_MAPS_API_KEY;
const mapId = import.meta.env.VITE_GOOGLE_MAPS_MAP_ID;
</script>
