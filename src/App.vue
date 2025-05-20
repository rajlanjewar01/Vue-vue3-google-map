<template>
  <div style="width: 800px">
    <GoogleMapComponent />
  </div>
</template>

<script>
import GoogleMapComponent from './components/GoogleMapComponent.vue';
export default {
  name: 'App',

  components: {
    GoogleMapComponent,
  },
};
</script>
