<template>
  <b-container class="outer" fluid>
    <b-container class="inner">
      <h3>How it works</h3>
      <b-row class="row" cols-lg="3">
        <b-col
          class="b-col"
          cols="8"
          offset="2"
          sm="6"
          offset-sm="0"
          md="6"
          lg="4"
        >
          <div class="description-box">
            <img src="../assets/icon-1.svg" alt="icon 1" />
            <p>
              You can now save the planet in style, thanks to cashback for your
              nespresso pods at any of our sixteen locations nationwide.
            </p>
          </div>
        </b-col>

        <b-col
          class="b-col"
          cols="8"
          offset="2"
          sm="6"
          offset-sm="0"
          md="6"
          lg="4"
        >
          <div class="description-box">
            <img src="../assets/icon-2.svg" alt="icon 2" />
            <p>
              Simply bring in your used pods, place them in an approved
              CoffeeDrop bag and bring them into store.
            </p>
          </div>
        </b-col>

        <b-col
          class="b-col"
          cols="8"
          offset="2"
          sm="6"
          offset-sm="3"
          md="6"
          offset-md="3"
          lg="4"
          offset-lg="0"
        >
          <div class="description-box not">
            <img src="../assets/icon-3.svg" alt="icon 3" />
            <p>
              Our trained staff will quickly calculate your cashback - or better
              still, you can do it yourself on our handy App available on iOS or
              Android
            </p>
          </div>
        </b-col>
      </b-row>
    </b-container>
  </b-container>
</template>

<script>
export default {
  name: "SectionDescription",
};
</script>

<style lang="scss" scoped>
.outer {
  min-height: 75vh;
  background-color: rgb(228, 228, 228);
  padding: 0;
}

.inner {
  height: 100%;
  min-width: 80%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  padding-top: 50px;

  h3 {
    text-align: center;
    font-weight: bold;
  }
}

.row {
  display: flex;
  align-items: center;
  justify-items: center;
}

.description-box {
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 30px;
  height: 500px;
  position: relative;

  img {
    width: 75%;
    min-width: 150px;
    max-width: 275px;
  }

  p {
    margin-top: 30px;
    text-align: center;
  }
}

.b-col {
  &:not(:nth-of-type(3))::after {
    content: "";
    background-image: url("../assets/arrow.svg");
    background-repeat: no-repeat;
    background-size: 100% 100%;
    background-position-y: 25%;
    position: absolute;
    top: 0;
    right: 0;
    width: 100px;
    height: 100px;
    margin-top: 25%;
    transform: translateX(50%);
  }
}

@media screen and (max-width: 990px) {
  .inner {
    min-width: 100%;
  }
}

@media screen and (max-width: 992px) {
  .b-col {
    &:not(:nth-of-type(3))::after {
      width: 80px;
      height: 80px;
      margin-top: 30%;
    }

    &:not(:nth-of-type(1))::after {
      display: none;
    }
  }

  .description-box {
    height: auto;
  }
}

@media screen and (max-width: 576px) {
  .b-col {
    &:first-of-type::after {
      display: none;
    }
  }
}
</style>
