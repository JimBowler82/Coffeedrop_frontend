<template>
  <div id="map" style="">
    <!--In the following div the HERE Map will render-->
    <div
      id="mapContainer"
      style="height: 100%; width: 100%"
      ref="hereMap"
    ></div>
  </div>
</template>

<script>
export default {
  name: "HereMap",
  props: {
    center: Object,
    // center object { lat: 40.730610, lng: -73.935242 }
  },
  data() {
    return {
      platform: null,
      apikey: "IhtkIaClMw1piLoY1dYC6btfraCYRbphRZQLo9zSf68",
      // You can get the API KEY from developer.here.com
    };
  },
  async mounted() {
    // Initialize the platform object:
    const platform = new window.H.service.Platform({
      apikey: this.apikey,
    });
    this.platform = platform;
    this.initializeHereMap();
  },
  methods: {
    initializeHereMap() {
      // rendering map

      const mapContainer = this.$refs.hereMap;
      const H = window.H;
      // Obtain the default map types from the platform object
      var maptypes = this.platform.createDefaultLayers();

      // Instantiate (and display) a map object:
      var map = new H.Map(mapContainer, maptypes.vector.normal.map, {
        zoom: 5.5,
        center: this.center,
      });

      var xxxx = require("../assets/map-pin.svg");

      var icon = new H.map.Icon(xxxx),
        coords = { lat: 51.54, lng: -0.4 },
        marker = new H.map.Marker(coords, { icon: icon });

      map.addObject(marker);

      addEventListener("resize", () => map.getViewPort().resize());
    },
  },
};
</script>

<style lang="scss" scoped>
#map {
  height: 100%;
  width: 100%;
  margin: 0;
  text-align: center;
  background-color: #ccc;
  position: relative;
}

canvas {
  width: 100%;
  height: 100%;
}
</style>
