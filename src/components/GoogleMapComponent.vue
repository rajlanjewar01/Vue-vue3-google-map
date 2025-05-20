<template>
  <GoogleMap
    :api-key="getGoogleMapKeys"
    :mapId="getMapId"
    class="my-map"
    :center="center"
    :zoom="15"
  >
    <AdvancedMarker :options="markerOptions" :pin-options="pinOptions" />
  </GoogleMap>
</template>

<script>
import { GoogleMap, AdvancedMarker } from 'vue3-google-map';

export default {
  name: 'GoogleMapComponent',

  components: {
    GoogleMap,
    AdvancedMarker,
  },

  data() {
    return {
      center: { lat: 40.689247, lng: -74.044502 },
      markerOptions: { position: this.center, title: 'LADY LIBERTY' },
      pinOptions: { background: '#FBBC04' },
    };
  },

  computed: {
    getGoogleMapKeys() {
      return import.meta.env.VITE_GOOGLE_API_KEY;
    },

    getMapId() {
      return import.meta.env.VITE_DEMO_MAP_ID;
    },
  },
};
</script>

<style scoped>
.my-map {
  width: 100%;
  height: 600px;
}
</style>
