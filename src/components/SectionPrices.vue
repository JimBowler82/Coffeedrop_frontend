<template>
  <b-container class="outer" fluid>
    <b-container class="inner">
      <h3>Prices</h3>
      <b-row class="row">
        <PriceCard
          v-for="priceDetails in priceCardContent"
          :key="priceDetails.id"
          :priceDetails="priceDetails"
        />
      </b-row>
    </b-container>
  </b-container>
</template>

<script>
import PriceCard from "./PriceCard.vue";
import { priceCardContent } from "../data/data";

export default {
  name: "SectionPrices",
  components: {
    PriceCard,
  },
  data() {
    return {
      priceCardContent: priceCardContent,
    };
  },
};
</script>

<style lang="scss" scoped>
.outer {
  @extend %outer;
  background-color: $background-dark;
}

.inner {
  @extend %inner;
  min-height: inherit;
  justify-content: center;

  h3 {
    @extend %inner-h3;
    color: $heading-light;
    margin-bottom: 50px;
  }
}

.row {
  width: 100%;
  max-width: 1200px;
  margin: 10px auto;
}

@media screen and (max-width: 990px) {
  .inner {
    min-width: 100%;
  }
}

@media screen and (max-width: 768px) {
  .inner h3 {
    margin: 30px 0;
  }

  .row {
    margin: 0;
  }
}
</style>
