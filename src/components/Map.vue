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
  @extend %outer;
  height: 75vh;
}

.inner {
  @extend %inner;
  min-width: 100%;
  justify-content: center;
  padding: 0px;
}
</style>
