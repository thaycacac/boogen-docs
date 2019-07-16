<template>
  <div class="navbar">
    <div class="container">
      <div class="navbar-link">
        <a href="#" class="navbar-logo">
          <img src="~/static/logo.png" width="40">
          Bootstrap Studio
        </a>
      </div>
      <div class="navbar-menu d-none d-sm-block">
        <a href="#" class="btn btn-primary btn-purchase navbar-right">Purchase</a>

        <ul class="navbar-right">
          <li class="menu-item">
            <a href="#">Features</a>
          </li>
          <li class="menu-item">
            <a href="#">Extras</a>
          </li>
          <li class="menu-item">
            <a href="#">Tutorials</a>
          </li>
          <li class="menu-item">
            <a href="#">Forums</a>
          </li>
        </ul>
      </div>
    </div>
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
.navbar {
  background-color: $color-gray-900;
  height: 70px;
  top: 0;
  position: fixed;
  width: 100%;
  z-index: 9;
  .navbar-logo {
    color: $color-white;
    font-size: 20px;
    margin-left: -15px;
  }
  .navbar-logo:hover {
    text-decoration: none !important;
  }
  .navbar-right {
    display: block;
    float: right;
    li {
      float: left;
      color: $color-white;
      padding: 10px 15px;
    }
    .menu-item a {
      color: $color-white;
    }
  }
  .btn-purchase {
    border-radius: 17px;
    padding: 9px;
    font-weight: 700;
  }
}
</style>
