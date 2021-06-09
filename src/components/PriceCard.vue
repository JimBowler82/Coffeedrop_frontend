<template>
  <b-col class="price-card b-col" cols="12" sm="6" md="4" order-md="0">
    <div>
      <h4>{{ priceDetails.title }}</h4>
      <ul>
        <li>Ristretto = {{ priceDetails.prices[0] }}p</li>
        <li>Espresso = {{ priceDetails.prices[1] }}p</li>
        <li>Lungo = {{ priceDetails.prices[2] }}p</li>
      </ul>
    </div>
  </b-col>
</template>

<script>
export default {
  name: "PriceCard",
  props: {
    priceDetails: Object,
  },
};
</script>

<style lang="scss" scoped>
.price-card {
  @include flex(column, flex-start, center);
  margin-bottom: 20px;

  div {
    @include flex(column, space-between, center);
    height: 300px;
    width: 90%;
    min-width: 200px;
    position: relative;

    &::after {
      content: url("../assets/images/coffee-beans.svg");
      position: absolute;
      bottom: 0;
      left: 50%;
      transform: translate(-50%, 40%);
    }
  }

  h4 {
    text-align: center;
    color: $green;
    width: 100%;
    font-weight: 600;
    margin-top: 20px;
  }

  ul {
    width: 100%;
    min-width: 200px;
    background-color: lighten($background-dark, 10);
    border-radius: 5px;
    list-style: none;
    padding: 0;
  }

  li {
    color: $heading-light;
    width: 100%;
    padding: 20px 0 20px 40px;

    &:nth-child(2) {
      background-color: lighten($gray, 25);
      border-radius: 5px;
    }
  }
}
</style>
