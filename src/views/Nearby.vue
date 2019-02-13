<template>
    <div> 
        <h2>Ho </h2>
        <Near />
        <input type="text" v-model="query">
    <button type="button" v-on:click="search()">Search</button>
    <Near 
      ref="map"
      appId="ZdhLpE0iq6OshZeRv80I"
      appCode="8C3WocTbllFZBwCMqqimQQ"
      v-bind:lat="lat"
      v-bind:lng="lng"
      width="100%"
      height="835px"
    />
    </div>
</template>


<script>
import Near from '@/components/Near.vue'

export default {
    name : 'Nearby',
    components : {
        Near
    },
    data() {
    return {
      lat: "33.577949499999995",
      lng: "-7.5857673000000005",
      query: "El Manar El Hank"
    };
  },
  mounted() {
    this.localisation();
    this.search();
  },
  methods: {
    localisation() {
      var latitude;
      var longitude;
      if (navigator.geolocation) {
        navigator.geolocation.getCurrentPosition(function(position) {
          latitude = position.coords.latitude;
          longitude = position.coords.longitude;

          console.log(
            "App" + "latitude : " + latitude + " longitude : " + longitude
          );
          console.log(typeof longitude);
        });
        setTimeout(function() {
          this.lat = "" + latitude;
          this.lng = "" + longitude;
          console.log(this.lat);
        }, 3000);
      }
    },
    search() {
      this.$refs.map.places(this.query);
    }
  }
}
</script>
