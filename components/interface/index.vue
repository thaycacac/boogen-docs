<template>
  <div class="interface">
    <h3 class="title">
      {{ title }}
    </h3>
    <p class="description">
      {{ description }}
    </p>
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
export default {
  data() {
    return {
      title: 'The Interface',
      description:
        'Bootstrap Studio has a beautiful and powerful interface, which is built around the simplicity of drag and drop. This makes it the perfect tool for prototyping and designing web pages and apps.',
    }
  },
}
</script>

<style lang="scss" scoped>
@import '~/assets/scss/_variables.scss';
@import '~/assets/scss/_sizes.scss';
@import '~/assets/scss/_mixins.scss';

$width-unit: 25px;

.interface {
  padding: $width-unit * 2 0px;
  .title {
    @include title-700;
    @include text-center;
    margin-bottom: $margin-unit;
  }
  .description {
    @include text-muted(#59697d);
    max-width: $max-width-unit;
    @media (max-width: 575.98px) {
      @include container;
    }
  }
  .interface-img {
    position: relative;
    .img-responsive {
      @include full-size;
      @include box-shadow;
    }
    .circle {
      width: $width-unit;
      height: $width-unit;
      background: linear-gradient(135deg, #6d90fb, #335fe9);
      border-radius: 50%;
      position: absolute;
      top: $width-unit * 1.2;
      left: 55%;
    }
    .ringring {
      animation: pulsate 2s ease-out;
      animation-iteration-count: infinite;
      @include circle-pulsate;
    }
  }

  @keyframes pulsate {
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
 