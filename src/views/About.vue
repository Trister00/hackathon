<template>
  <div id="app">
    <Adresse
      ref="map"
      appId="ZdhLpE0iq6OshZeRv80I"
      appCode="8C3WocTbllFZBwCMqqimQQ"
      v-bind:lat="lat"
      v-bind:lng="lng"
      width="100%"
      height="835px"
      location="Beauséjour ,Casablanca"
    />
  </div>
</template>

<script>
import Adresse from "@/components/Adresse.vue";

export default {
  name: "app",
  components: {
    Adresse
  },
  data() {
    return {
      lat: "33.577949499999995",
      lng: "-7.5857673000000005"
    };
  }
};
</script>