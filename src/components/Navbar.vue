<template>
  <div>
    <b-navbar toggleable="lg" type="dark">
      <b-navbar-brand href="#">
        <img src="../assets/images/logo.svg" alt="CoffeeDrop Logo" />
      </b-navbar-brand>

      <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

      <b-collapse id="nav-collapse" is-nav class="ml-auto">
        <b-navbar-nav>
          <b-nav-item href="#">Login</b-nav-item>
          <b-nav-item href="#">Download IOS App</b-nav-item>
          <b-nav-item href="#">Download Android App</b-nav-item>
        </b-navbar-nav>

        <!-- Right aligned nav items -->
        <b-navbar-nav class="ml-auto"> </b-navbar-nav>
      </b-collapse>
    </b-navbar>
  </div>
</template>

<script>
export default {
  name: "Navbar",
};
</script>

<style lang="scss" scoped>
div {
  padding-top: 20px;

  .navbar-collapse {
    flex-grow: 0;
  }
  .navbar-dark .navbar-nav .nav-link {
    color: white;
    margin-left: 80px;
    &:hover {
      color: $green;
    }
  }
}
</style>
