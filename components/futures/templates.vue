<template>
  <div class="templates">
    <h3 class="title">
      {{ title }}
    </h3>
    <p class="description">
      {{ description }}
    </p>
    <div class="slide">
      <b-carousel
        id="carousel-template"
        v-model="slide"
        :interval="3000"
        controls
        indicators
        style="text-shadow: 1px 1px 2px #333;"
        @sliding-start="onSlideStart"
        @sliding-end="onSlideEnd"
      >
        <b-carousel-slide class="slide-item">
          <img
            slot="img"
            class="d-block img-fluid w-100"
            :src="require('@/assets/images/header/slider1.png')"
            alt="image slot"
          >
        </b-carousel-slide>
        <b-carousel-slide class="slide-item">
          <img
            slot="img"
            class="d-block img-fluid w-100"
            :src="require('@/assets/images/header/slider1.png')"
            alt="image slot"
          >
        </b-carousel-slide>
        <b-carousel-slide class="slide-item">
          <img
            slot="img"
            class="d-block img-fluid w-100"
            :src="require('@/assets/images/header/slider1.png')"
            alt="image slot"
          >
        </b-carousel-slide>
      </b-carousel>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      title: 'Beautiful Templates',
      description:
        'The app comes with a number of premium, fully responsive templates that you can customize. Each template consists of multiple pages and widgets you can pick-and-match into the perfect website.',
      slide: 0,
      sliding: null,
    }
  },
  methods: {
    onSlideStart(slide) {
      this.sliding = true
    },
    onSlideEnd(slide) {
      this.sliding = false
    },
  },
}
</script>

<style lang="scss" scoped>
@import '~/assets/scss/_variables.scss';
@import '~/assets/scss/_sizes.scss';
@import '~/assets/scss/_mixins.scss';

.templates {
  background-color: $color-blue;
  color: $color-white;
  padding-top: $padding-unit;
  .title {
    @include title-700;
    @include text-center;
  }
  .description {
    @include text-muted(#fff);
    max-width: $max-width-unit;
    @media (max-width: 575.98px) {
      padding-top: $padding-unit;
      @include container;
    }
  }
  .slide {
    max-width: $max-width-unit * 1.6;
    margin: 0px auto;
    padding-bottom: $padding-unit;
    @media (max-width: 767.98px) {
      @include container;
    }
  }
}
</style>

