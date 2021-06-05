<template>
  <b-container class="outer" fluid>
    <b-container class="inner">
      <h3>How it works</h3>
      <b-row class="row">
        <b-col>
          <div class="description-box">
            <img src="../assets/icon-1.svg" alt="icon 1" />
            <p>
              You can now save the planet in style, thanks to cashback for your
              nespresso pods at any of our sixteen locations nationwide.
            </p>
          </div>
        </b-col>
        <b-col class="arrow">
          <img src="../assets/arrow.svg" alt="arrow" />
        </b-col>
        <b-col>
          <div class="description-box">
            <img src="../assets/icon-2.svg" alt="icon 2" />
            <p>
              Simply bring in your used pods, place them in an approved
              CoffeeDrop bag and bring them into store.
            </p>
          </div>
        </b-col>
        <b-col class="arrow">
          <img src="../assets/arrow.svg" alt="arrow" />
        </b-col>
        <b-col>
          <div class="description-box">
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
  height: 75vh;
  background-color: rgb(228, 228, 228);
}

.inner {
  height: 100%;
  min-width: 80%;
  display: flex;
  flex-direction: column;
  justify-content: center;

  h3 {
    text-align: center;
    font-weight: bold;
  }
}

.row {
  display: flex;
  align-items: center;
  justify-items: center;

  .arrow {
    align-self: flex-start;
    transform: translateY(225%);
    display: flex;
    max-width: 70px;
    padding: 0;
    margin: 0;
  }
}

.description-box {
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 30px;
  height: 500px;
  width: 100%;

  img {
    width: 200px;
  }

  p {
    margin-top: 30px;
    text-align: center;
  }
}
</style>
