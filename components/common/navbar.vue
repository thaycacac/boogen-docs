<template>
  <b-navbar toggleable="lg" type="dark">
    <b-container>
      <b-navbar-brand href="#">
        <img src="~/static/logo.png" width="25">
        Boogen
      </b-navbar-brand>
      <b-navbar-toggle target="nav-collapse" />
      <b-collapse id="nav-collapse" is-nav>
        <b-navbar-nav class="ml-auto">
          <b-nav-item href="#" class="my-nav-link">
            Features
          </b-nav-item>
          <b-nav-item href="#">
            Tutorials
          </b-nav-item>
          <b-nav-item href="#">
            Forums
          </b-nav-item>
          <b-button variant="primary" pill>
            Purchase
          </b-button>
        </b-navbar-nav>
      </b-collapse>
    </b-container>
  </b-navbar>
</template>

<style lang="scss" scoped>
@import '~/assets/scss/_variables.scss';

.navbar {
  background-color: $color-gray-900;
  height: 60px;
  top: 0;
  position: fixed;
  width: 100%;
  z-index: 999;
  .nav-link {
    color: $color-white;
    padding-right: 0.8rem;
    padding-left: 0.8rem;
  }
  .my-nav-link {
    color: $color-white;
  }
  .navbar-collapse {
    background-color: $color-gray-900;
    margin-left: -15px;
    border-top: 1px solid $color-gray-900;
  }
  @media (max-width: 575.98px) {
    .navbar-collapse {
      padding-bottom: 1.5rem;
    }
  }
  @media (max-width: 787.98px) {
    .navbar-collapse {
      padding-bottom: 1.5rem;
    }
  }
}
</style>
