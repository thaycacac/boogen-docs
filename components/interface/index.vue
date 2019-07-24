<template>
  <div class="interface">
    <h3>The Interface</h3>
    <p>Bootstrap Studio has a beautiful and powerful interface, which is built around the simplicity of drag and drop. This makes it the perfect tool for prototyping and designing web pages and apps.</p>
    <div class="container interface-img">
      <img
        :src="require('@/assets/images/home/header.jpg')"
        class="img-responsive"
        alt="image background"
      >
      <div v-b-tooltip.hover class="ringring d-none d-xl-block" title="Tooltip content" />
      <div class="circle d-none d-xl-block" />
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
@import '~/assets/scss/main.scss';
.interface {
  padding: 50px 0px;
  h3 {
    font-weight: 700;
    text-align: center;
    font-size: 36px;
    margin-bottom: 40px;
  }
  p {
    text-align: center;
    font-size: 18px;
    color: #59697d;
    line-height: 1.5;
    margin: 0 auto 50px;
    max-width: 600px;
    font-weight: 400;
  }
  .interface-img {
    position: relative;
  }
  .img-responsive {
    width: 100%;
    box-shadow: 0 2px 5px rgba(0, 0, 0, 0.15);
  }
  .circle {
    width: 25px;
    height: 25px;
    background: linear-gradient(135deg, #6d90fb, #335fe9);
    border-radius: 50%;
    position: absolute;
    top: 30px;
    left: 55%;
  }

  .ringring {
    border: 10px solid #8abdb8;
    -webkit-border-radius: 30px;
    height: 30px;
    width: 30px;
    position: absolute;
    top: 28px;
    left: 54.9%;
    -webkit-animation: pulsate 2s ease-out;
    -webkit-animation-iteration-count: infinite;
    opacity: 0;
  }
  @-webkit-keyframes pulsate {
    0% {
      -webkit-transform: scale(0.1, 0.1);
      opacity: 0;
    }
    50% {
      opacity: 1;
    }
    100% {
      -webkit-transform: scale(1.2, 1.2);
      opacity: 0;
    }
  }
}
</style>
 