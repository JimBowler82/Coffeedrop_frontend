<template>
  <b-container class="outer" fluid>
    <b-container class="inner">
      <p>This app is powered by</p>
      <img src="../assets/footer-logo.svg" alt="footer logo" />
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
  background-color: #373737;
}

.inner {
  height: 100%;
  min-width: 80%;
  display: flex;
  flex-direction: column;
  justify-content: center;

  p {
    text-align: center;
    color: white;
    margin: 0;
    letter-spacing: 1px;
  }

  img {
    width: 225px;
    margin: 0 auto;
  }
}
</style>
