<template>
  <a :href="appStore.url">
    <img
      :src="require(`../assets/images/${appStore.img}`)"
      :alt="appStore.alt"
    />
  </a>
</template>

<script>
export default {
  name: "ApStoreButton",
  props: {
    appStore: Object,
  },
};
</script>

<style lang="scss" scoped>
a img {
  width: 200px;

  &:first-of-type {
    margin-right: 30px;
  }
}

@media screen and (max-width: 990px) {
  a {
    img {
      &:first-of-type {
        margin-bottom: 15px;
      }
    }
  }
}
</style>
