<template>
  <b-container id="app" fluid>
    <Header />
    <SectionDescription />
    <SectionPrices />
    <Map />
    <Footer />
  </b-container>
</template>

<script>
import Header from "./components/Header";
import SectionDescription from "./components/SectionDescription";
import SectionPrices from "./components/SectionPrices";
import Map from "./components/Map";
import Footer from "./components/Footer";

export default {
  name: "App",
  components: {
    Header,
    SectionDescription,
    SectionPrices,
    Map,
    Footer,
  },
};
</script>

<style lang="scss">
@import "./assets/scss/main.scss";

#app {
  box-sizing: border-box;
  font-family: $font-family;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  padding: 0;
  margin: 0;
}
</style>
