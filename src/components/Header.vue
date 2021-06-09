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
            <AppStoreButton
              v-for="appStore in appStoreButtons"
              :key="appStore.id"
              :appStore="appStore"
            />
          </div>
        </div>

        <div class="app-mockup">
          <img
            src="../assets/images/app-mockup@2x.png"
            alt="app mockup illustration"
          />
        </div>
      </div>
    </b-container>
  </b-container>
</template>

<script>
import Navbar from "./Navbar.vue";
import AppStoreButton from "./AppStoreButton.vue";
import { appStoreButtons } from "../data/data";
export default {
  name: "Header",
  components: {
    Navbar,
    AppStoreButton,
  },
  data() {
    return {
      appStoreButtons: appStoreButtons,
    };
  },
};
</script>

<style lang="scss" scoped>
.outer {
  @extend %outer;
  background-image: url("../assets/images/coffeebeans-1.jpg");
  background-size: cover;
  background-position: center;
  height: 75vh;
}

.inner {
  @extend %inner;
}

.headline {
  color: $heading-light;
  display: flex;
  height: 100%;
}

.headline-description {
  display: flex;
  flex-direction: column;
  width: 50%;
  color: $heading-light;

  h1 {
    font-weight: 700;
    margin-top: 100px;
  }

  h3 {
    font-weight: 300;
    margin-top: 50px;
    font-weight: 400;
  }
}

.app-store-buttons {
  display: flex;
  margin-top: 60px;
}

.app-mockup {
  width: 50%;
  height: 100%;
  display: flex;
  justify-content: start;
  align-items: flex-end;

  img {
    width: 800px;
    transform: translateX(-100px);
  }
}

@media screen and (max-width: 990px) {
  .inner {
    min-width: 100%;
  }

  .app-store-buttons {
    flex-direction: column;
    margin-top: 30px;
  }
}

@media screen and (max-width: 800px) {
  .outer {
    min-height: 100vh;
  }
  .headline {
    flex-direction: column;
  }

  .headline-description {
    width: 100%;

    h1 {
      margin-top: 20px;
    }
  }

  .app-mockup {
    width: 100%;

    img {
      transform: translate(10px, -80px);
    }
  }
}

@media screen and (max-width: 576px) {
  .headline-description {
    h3 {
      display: none;
    }
  }

  .app-mockup {
    img {
      transform: translate(-200px, 0px);
    }
  }
}
</style>
