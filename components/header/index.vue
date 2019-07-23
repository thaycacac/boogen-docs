<template>
  <div class="wrap-all">
    <div class="container">
      <b-row class="wrap-top">
        <b-col class="d-flex justify-content-center flex-column">
          <h2 class="title font-weight-bold">
            Bootstrap 4 builder
          </h2>
          <h1 class="large font-weight-light mt-3 mb-4">
            Design, build and deploy web pages in a flow.
          </h1>
          <h3
            class="small font-weight-light"
          >
            Pingendo is a modern tool for designers, developers and web agencies. Intuitive as stacking blocks, powerful as a text editor.
          </h3>
          <b-button squared variant="primary mt-3 button">
            Download it for free
          </b-button>
        </b-col>
        <b-col class="wrap-slide d-flex flex-column justify-content-center">
          <img :src="require('@/assets/images/header/slider1.png')" alt="image slide 1" class="slide-1 position-absolute">
          <img :src="require('@/assets/images/header/slider2.png')" alt="image slide 2" class="slide-2 position-absolute">
          <img :src="require('@/assets/images/header/slider3.png')" alt="image slide 3" class="slide-3 position-absolute">
        </b-col>
      </b-row>
    </div>
  </div>
</template>

<script>
export default {}
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
    height: calc(100vh - 30px);
  }
}

.wrap-slide {
  transform: perspective(1000px) rotateY(-20deg) translateX(-20px);
  .slide-1 {
    width: 500px;
    animation: slide-1 7s ease-in-out infinite;
    @include box-shadow;
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
}

.small {
  font-size: $unit;
}

.button {
  width: 220px;
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

