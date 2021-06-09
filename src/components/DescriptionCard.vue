<template>
  <b-col class="b-col" cols="8" offset="2" sm="6" offset-sm="0" md="6" lg="4">
    <div class="description-box">
      <img
        :src="require(`../assets/images/${description.img}`)"
        :alt="description.imgAlt"
      />
      <p>{{ description.content }}</p>
    </div>
  </b-col>
</template>
<script>
export default {
  name: "DescriptionCard",
  props: {
    description: Object,
  },
};
</script>

<style lang="scss" scoped>
.description-box {
  @include flex(column, flex-start, center);
  padding: 30px;
  height: 500px;
  position: relative;

  img {
    width: 75%;
    min-width: 150px;
    max-width: 250px;
  }

  p {
    margin-top: 30px;
    text-align: center;
    color: $paragraph-text;
    font-size: 1.2rem;
    font-weight: 400;
    width: 90%;
  }
}

.b-col {
  &:not(:nth-of-type(3))::after {
    content: "";
    background-image: url("../assets/images/arrow.svg");
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
