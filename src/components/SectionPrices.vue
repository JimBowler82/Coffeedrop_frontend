<template>
  <b-container class="outer" fluid>
    <b-container class="inner">
      <h3>Prices</h3>
      <b-row class="row">
        <b-col class="price-card b-col" cols="12" sm="6" md="4" order-md="0">
          <div>
            <h4>The first 50 capsules:</h4>
            <ul>
              <li>Ristretto = 2p</li>
              <li>Espresso = 4p</li>
              <li>Lungo = 6p</li>
            </ul>
          </div>
        </b-col>
        <b-col class="price-card b-col" cols="12" sm="6" md="4" order-md="0">
          <div>
            <h4>Capsules 50-500:</h4>
            <ul>
              <li>Ristretto = 3p</li>
              <li>Espresso = 6p</li>
              <li>Lungo = 9p</li>
            </ul>
          </div>
        </b-col>
        <b-col
          class="price-card b-col"
          cols="12"
          sm="6"
          offset-sm="3"
          md="4"
          offset-md="0"
          order-md="0"
        >
          <div>
            <h4>Capsules 501+:</h4>
            <ul>
              <li>Ristretto = 5p</li>
              <li>Espresso = 10p</li>
              <li>Lungo = 15p</li>
            </ul>
          </div>
        </b-col>
      </b-row>
    </b-container>
  </b-container>
</template>

<script>
export default {
  name: "SectionPrices",
};
</script>

<style lang="scss" scoped>
.outer {
  background-color: #373737;
  min-height: 75vh;
  padding: 0;
}

.inner {
  min-height: inherit;
  min-width: 80%;
  display: flex;
  flex-direction: column;
  justify-content: center;

  h3 {
    text-align: center;
    font-weight: bold;
    color: white;
    margin-bottom: 50px;
  }
}

.row {
  width: 100%;
  max-width: 1200px;
  margin: 10px auto;
}

.price-card {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin-bottom: 20px;

  div {
    height: 300px;
    width: 90%;
    min-width: 200px;
    position: relative;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    align-items: center;

    &::after {
      content: url("../assets/coffee-beans.svg");
      position: absolute;
      bottom: 0;
      left: 50%;
      transform: translate(-50%, 40%);
    }
  }

  h4 {
    text-align: center;
    color: #29e7a9;
    width: 100%;
    margin-top: 20px;
  }

  ul {
    width: 100%;
    min-width: 200px;
    background-color: #4e4e4e;
    border-radius: 5px;
    list-style: none;
    padding: 0;
  }

  li {
    color: white;
    width: 100%;
    padding: 20px 0 20px 40px;

    &:nth-child(2) {
      background-color: #626262;
      border-radius: 5px;
    }
  }
}

@media screen and (max-width: 990px) {
  .inner {
    min-width: 100%;
  }
}

@media screen and (max-width: 768px) {
  .inner h3 {
    margin: 30px 0;
  }

  .row {
    margin: 0;
  }
}
</style>
