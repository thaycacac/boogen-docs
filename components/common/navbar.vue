<template>
  <div>
    <b-navbar toggleable="lg" type="dark">
      <b-container>
        <b-navbar-brand href="#">
          <img src="~/static/logo.png" width="40">
          Bootstrap Studio
        </b-navbar-brand>
        <b-navbar-toggle target="nav-collapse" />
        <b-collapse id="nav-collapse" is-nav>
          <b-navbar-nav class="ml-auto">
            <b-nav-item href="#">
              Features
            </b-nav-item>
            <b-nav-item-dropdown text="Extras" right>
              <b-dropdown-item href="#">
                Sites Platform
              </b-dropdown-item>
              <b-dropdown-item href="#">
                Smart Forms
              </b-dropdown-item>
            </b-nav-item-dropdown>
            <b-nav-item href="#">
              Tutorials
            </b-nav-item>
            <b-nav-item href="#">
              Forums
            </b-nav-item>
            <b-button variant="primary purchase" pill>
              Purchase
            </b-button>
          </b-navbar-nav>
        </b-collapse>
      </b-container>
    </b-navbar>
  </div>
</template>

<style lang="scss" scoped>
@import '~/assets/scss/main.scss';

ul {
  list-style: none;
}
a:hover {
  text-decoration: none;
}
.navbar-dark .navbar-nav .nav-link {
  color: $color-white !important;
}
.navbar {
  background-color: $color-gray-900;
  height: 70px;
  top: 0;
  position: fixed;
  width: 100%;
  z-index: 9;
  .nav-link {
    color: $color-white;
    padding-right: 0.8rem;
    padding-left: 0.8rem;
  }
  .purchase {
    font-weight: 700;
  }
  .navbar-collapse {
    background-color: $color-gray-900;
    margin-left: -15px;
    border-top: 1px solid $color-gray-900;
    margin-top: 10px;
  }
  @media (max-width: 575.98px) {
    .navbar-collapse {
      padding-bottom: 1.5rem;
      .purchase {
        width: 7rem;
        margin-left: 15px;
      }
    }
  }
  @media (max-width: 787.98px) {
    .navbar-collapse {
      padding-bottom: 1.5rem;
      .purchase {
        width: 7rem;
        margin-left: 15px;
      }
    }
  }
}
</style>
