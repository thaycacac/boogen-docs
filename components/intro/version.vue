<template>
  <div class="version">
    <section class="centered">
      <h3 class="title">
        <i class="far fa-check-circle icon-check d-none d-xl-block" />
        <strong>{{ strong }}</strong>
        {{ text }}
        <a href="#" target="_blank">{{ link }}</a>
      </h3>
      <div class="youtube">
        <iframe
          class="responsive-youtube"
          src="https://www.youtube.com/embed/EUEUZDV-in0?list=RDEUEUZDV-in0"
          frameborder="0"
          allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture"
        />
      </div>
    </section>
  </div>
</template>

<script>
export default {
  data() {
    return {
      strong: 'Bootstrap Studio 4.5.2',
      text: "is here! See what's new on our",
      link: 'releases page »',
    }
  },
}
</script>

<style lang="scss" scoped>
@import '~/assets/scss/_variables.scss';
@import '~/assets/scss/_sizes.scss';
@import '~/assets/scss/_mixins.scss';

$font-weght: 350;
.version {
  background-color: $color-gray-200;
  @media (max-width: 767.98px) {
    @include container;
  }
  section {
    padding-top: $padding-unit * 1.5;
    max-width: $max-width-unit * 1.34;
    margin: 0 auto;
    @media (max-width: 767.98px) {
      padding-top: $padding-unit;
    }
    .title {
      max-width: $max-width-unit * 1.11;
      margin: 0 auto 50px;
      line-height: 1.45;
      font-size: $unit * 1.56;
      text-align: left;
      font-weight: $font-weght;

      @media (max-width: 767.98px) {
        @include text-center;
      }
      .icon-check {
        font-size: $unit * 3.5;
        font-weight: $font-weght * 2;
        @include icon-left;
      }
    }
    .youtube {
      padding-bottom: $padding-unit * 0.75;
      height: $max-width-unit * 0.75;
      @media (max-width: 575.98px) {
        height: $max-width-unit * 0.38 !important;
      }
      @media (max-width: 767.98px) {
        height: $max-width-unit * 0.58 !important;
      }
      .responsive-youtube {
        @include full-size;
      }
    }
  }
}
</style>
