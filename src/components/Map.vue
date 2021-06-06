<template>
  <b-container class="outer" fluid>
    <b-container class="inner">
      <HereMap :center="center" />
    </b-container>
  </b-container>
</template>

<script>
import HereMap from "./HereMap.vue";

export default {
  name: "Map",
  data() {
    return {
      center: { lat: 52.934931, lng: 4.895098 },
    };
  },
  components: {
    HereMap,
  },
};
</script>

<style lang="scss" scoped>
.outer {
  height: 75vh;
  padding: 0px;
}

.inner {
  height: 100%;
  min-width: 100%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  padding: 0px;

  h3 {
    text-align: center;
  }
}
</style>
