<template>
  <div class="wrap-all">
    <div class="container">
      <b-row class="wrap-top">
        <b-col class="d-flex justify-content-center flex-column" sm="12" xs="12" md="6" lg="6">
          <h2 class="title font-weight-bold">
            {{ title }}
          </h2>
          <h1 class="large font-weight-light mt-3 mb-4">
            {{ slogan }}
          </h1>
          <h3
            class="small font-weight-light"
          >
            {{ description }}
          </h3>
          <b-button squared variant="primary mt-3 button">
            Download it for free
          </b-button>
        </b-col>
        <b-col class="wrap-slide d-flex flex-column justify-content-center" sm="12" xs="12" md="6" lg="6">
          <img
            :src="require('@/assets/images/header/slider1.png')"
            alt="image slide 1"
            class="slide-1"
          >
          <img
            :src="require('@/assets/images/header/slider2.png')"
            alt="image slide 2"
            class="slide-2 position-absolute hidden-md-down"
          >
          <img
            :src="require('@/assets/images/header/slider3.png')"
            alt="image slide 3"
            class="slide-3 position-absolute hidden-md-down"
          >
        </b-col>
      </b-row>
      <b-row class="wrap-bottom">
        <b-col>Work with</b-col>
        <b-col>
          <img
            :src="require('@/assets/images/header/bootstrap.png')"
            alt="logo bootstrap"
            class="image-oran"
          >
        </b-col>
        <b-col>
          <img
            :src="require('@/assets/images/header/sass.png')"
            alt="logo sass"
            class="image-oran"
          >
        </b-col>
      </b-row>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      title: 'Bootstrap 4 builder',
      slogan: 'Design, build and deploy web pages in a flow.',
      description: 'Pingendo is a modern tool for designers, developers sand web agencies. Intuitive as stacking blocks, powerful as a text editor.'
    }
  }
}
</script>

<style lang="scss" scoped>
@import '~/assets/scss/_variables.scss';
@import '~/assets/scss/_sizes.scss';
@import '~/assets/scss/_mixins.scss';

$height: 100vh;

.wrap-all {
  height: $height;
  background: url('~assets/images/header/background.jpg');
  background-size: cover;
  .wrap-top {
    height: calc(100vh - 50px);
  }
  .wrap-bottom {
    height: 50px;
  }
}

.wrap-slide {
  transform: perspective(1000px) rotateY(-20deg) translateX(-20px);
  @media (max-width: 768px) {
    transform: none;
  }
  .slide-1 {
    width: 500px;
    animation: slide-1 7s ease-in-out infinite;
    @include box-shadow;
    position: absolute;
    @media (max-width: 768px) {
      position: relative;
      width: 100%;
    }
  }
  .slide-2 {
    left: -40px;
    width: 90px;
    animation: slide-1 5s ease-in-out infinite;
    @include box-shadow;
  }
  .slide-3 {
    right: -85px;
    width: 230px;
    animation: slide-2 4s ease-in-out infinite;
    @include box-shadow;
  }
}

.title {
  font-size: $unit * 1.4;
  color: $color-primary;
  @media (max-width: 768px) {
    font-size: $unit;
  }
}

.small {
  font-size: $unit;
}

.button {
  width: 220px;
}

.image-oran {
  height: 30px;
}

.hidden-md-down {
  @media (max-width: 992px) {
    display: none;
  }
}

@keyframes slide-1 {
  0% {
    transform: translateX(0) translateY(5px);
  }
  50% {
    transform: translateX(0) translateY(-5px);
  }
  100% {
    transform: translateX(0) translateY(5px);
  }
}

@keyframes slide-2 {
  0% {
    transform: translateX(0) translateY(10px);
  }
  50% {
    transform: translateX(0) translateY(-10px);
  }
  100% {
    transform: translateX(0) translateY(10px);
  }
}
</style>
