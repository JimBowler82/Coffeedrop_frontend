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
      apikey: process.env.VUE_APP_HERE_MAP_KEY,
      locations: [],
    };
  },
  async mounted() {
    this.getlocationData(process.env.VUE_APP_COFFEE_DROP_LOCATIONS_URL);
    // Initialize the platform object:
    const platform = new window.H.service.Platform({
      apikey: this.apikey,
    });
    this.platform = platform;
  },
  methods: {
    async getlocationData(url) {
      const response = await fetch(url);
      const { data, links } = await response.json();
      this.locations = [...this.locations, ...data];

      if (links.next) {
        this.getlocationData(links.next);
      } else {
        this.initializeHereMap();
      }
    },
    initializeHereMap() {
      const mapContainer = this.$refs.hereMap;
      const H = window.H;
      const maptypes = this.platform.createDefaultLayers();

      const map = new H.Map(mapContainer, maptypes.vector.normal.map, {
        zoom: 5.5,
        center: this.center,
      });

      // Map marker svg
      const svg = require("../assets/images/map-pin.svg");

      // Place map marker for each location
      this.locations.forEach((location) => {
        const icon = new H.map.Icon(svg),
          coords = {
            lat: location.coordinates.latitude,
            lng: location.coordinates.longitude,
          },
          marker = new H.map.Marker(coords, { icon: icon });

        map.addObject(marker);
      });

      // Listen for resize
      addEventListener("resize", () => map.getViewPort().resize());

      // Allow moving around map behaviour
      //new H.mapevents.Behavior(new H.mapevents.MapEvents(map));
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
