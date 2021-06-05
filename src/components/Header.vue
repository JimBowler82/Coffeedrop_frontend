<template>
  <b-container class="outer" fluid>
    <b-container class="inner">
      <Navbar />
      <div class="headline">
        <div class="headline-description">
          <h1>
            Recycle your <br />
            Nespresso in style!
          </h1>
          <h3>
            We can recycle your coffee pods for <br />
            cashback or free coffee!
          </h3>
          <div class="app-store-buttons">
            <a href="#">
              <img
                src="../assets/app-store@2x.png"
                alt="IOS app store button"
              />
            </a>
            <a href="#">
              <img
                src="../assets/google-play@2x.png"
                alt="Google play button"
              />
            </a>
          </div>
        </div>

        <div class="app-mockup">
          <img
            src="../assets/app-mockup@2x.png"
            alt="app mockup illustration"
          />
        </div>
      </div>
    </b-container>
  </b-container>
</template>

<script>
import Navbar from "./Navbar.vue";
export default {
  name: "Header",
  components: {
    Navbar,
  },
};
</script>

<style lang="scss" scoped>
.outer {
  background-image: url("../assets/coffeebeans-1.jpg");
  background-repeat: no-repeat;
  background-size: 100%;
  height: 75vh;
}

.inner {
  min-width: 80%;
  height: 100%;
  display: flex;
  flex-direction: column;
}

.headline {
  color: white;
  display: flex;
  height: 100%;
}

.headline-description {
  display: flex;
  flex-direction: column;
  width: 50%;

  h1 {
    font-weight: 700;
    margin-top: 100px;
  }

  h3 {
    font-weight: 300;
    margin-top: 50px;
  }
}

.app-store-buttons {
  display: flex;
  margin-top: 60px;

  img {
    width: 200px;

    &:first-of-type {
      margin-right: 30px;
    }
  }
}

.app-mockup {
  width: 50%;
  display: flex;
  justify-content: start;
  align-items: flex-end;

  img {
    width: 800px;
    transform: translateX(-100px);
  }
}
</style>
