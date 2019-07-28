<template>
  <div class="realtime">
    <h3 class="title">
      {{ title }}
    </h3>
    <p class="description">
      {{ description }}
    </p>
    <div class="retro">
      <img
        :src="require('@/assets/images/home/real_time_preview.jpg')"
        alt="image"
        class="img-item"
      >
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      title: 'Realtime Preview',
      description:
        'Bootstrap Studio has a powerful feature called Preview. With it, you can open your design in multiple web browsers and devices, and every change you make within the app will be shown instantaneously everywhere. ',
    }
  },
}
</script>

<style lang="scss" scoped>
@import '~/assets/scss/_variables.scss';
@import '~/assets/scss/_sizes.scss';
@import '~/assets/scss/_mixins.scss';

.realtime {
  padding-top: $padding-unit;
  .title {
    @include title-700;
    text-align: center;
    color: $color-primary;
    padding-bottom: $padding-unit;
  }
  .description {
    @include text-muted($color-black);
    max-width: $max-width-unit;
    @media (max-width: 575.98px) {
      @include container;
    }
  }
  .retro{
    max-width: $max-width-unit;
    margin: $margin-unit * 0.5 auto;
    .img-item{
      width: 100%;
    }
  }
}
</style>

