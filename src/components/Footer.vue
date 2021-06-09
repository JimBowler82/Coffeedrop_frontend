<template>
  <b-container class="outer" fluid>
    <b-container class="inner">
      <p>This app is powered by</p>
      <img src="../assets/images/footer-logo.svg" alt="footer logo" />
    </b-container>
  </b-container>
</template>

<script>
export default {
  name: "Footer",
};
</script>

<style lang="scss" scoped>
.outer {
  height: 12vh;
  background-color: $background-dark;
}

.inner {
  @extend %inner;
  justify-content: center;

  p {
    text-align: center;
    color: $heading-light;
    margin: 0;
    letter-spacing: 1px;
  }

  img {
    width: 225px;
    margin: 0 auto;
  }
}
</style>
