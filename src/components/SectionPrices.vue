<template>
  <b-container class="outer" fluid>
    <b-container class="inner">
      <h3>Prices</h3>
      <b-row class="row">
        <b-col class="price-card">
          <div>
            <h4>The first 50 capsules:</h4>
            <ul>
              <li>Ristretto = 2p</li>
              <li>Espresso = 4p</li>
              <li>Lungo = 6p</li>
            </ul>
          </div>
        </b-col>
        <b-col class="price-card">
          <div>
            <h4>Capsules 50-500:</h4>
            <ul>
              <li>Ristretto = 3p</li>
              <li>Espresso = 6p</li>
              <li>Lungo = 9p</li>
            </ul>
          </div>
        </b-col>
        <b-col class="price-card">
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
  height: 75vh;
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
    color: white;
    margin-bottom: 50px;
  }
}

.price-card {
  height: 300px;
  display: flex;
  flex-direction: column;
  align-items: center;

  h4 {
    text-align: center;
    color: #29e7a9;
    margin-bottom: 20px;
  }

  div {
    width: 90%;
    position: relative;

    &::after {
      content: url("../assets/coffee-beans.svg");
      position: absolute;
      bottom: 0;
      left: 50%;

      transform: translate(-50%, 40%);
    }
  }

  ul {
    width: 100%;
  }

  ul {
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
</style>
