<template>
  <b-container class="outer" fluid>
    <b-container class="inner">
      <h3>How it works</h3>
      <b-row class="row" cols-lg="3">
        <DescriptionCard
          v-for="description in descriptionCardContent"
          :key="description.id"
          :description="description"
        />
      </b-row>
    </b-container>
  </b-container>
</template>

<script>
import { descriptionCardContent } from "../data/data";
import DescriptionCard from "./DescriptionCard.vue";

export default {
  name: "SectionDescription",
  components: {
    DescriptionCard,
  },
  data() {
    return {
      descriptionCardContent: descriptionCardContent,
    };
  },
};
</script>

<style lang="scss" scoped>
.outer {
  @extend %outer;
  background-color: $background-light;
}

.inner {
  @extend %inner;
  justify-content: center;
  padding-top: 50px;

  h3 {
    @extend %inner-h3;
    color: $heading-dark;
  }
}

.row {
  @include flex(row, flex-start, center);
  justify-items: center;
}

@media screen and (max-width: 990px) {
  .inner {
    min-width: 100%;
  }
}
</style>
