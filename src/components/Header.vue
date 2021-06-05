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
  width: 100%;
  background-image: url("../assets/coffeebeans-1.jpg");
  background-size: cover;
  background-position: center;
  height: 75vh;
  min-height: 75vh;
  padding: 0;
  overflow: hidden;
}

.inner {
  min-width: 80%;
  height: 100%;
  display: flex;
  flex-direction: column;
  border: 1px solid blue;
}

.headline {
  color: white;
  display: flex;
  height: 100%;
  border: 1px solid red;
}

.headline-description {
  display: flex;
  flex-direction: column;
  width: 50%;
  border: 1px solid green;

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
  height: 100%;
  display: flex;
  justify-content: start;
  align-items: flex-end;
  border: 1px solid yellow;

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

    img {
      &:first-of-type {
        margin-bottom: 15px;
      }
    }
  }

  .app-mockup {
    img {
      width: 650px;
      transform: translateX(-150px);
    }
  }
}

@media screen and (max-width: 800px) {
  .outer {
    height: auto;
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
    }
  }
}
</style>
