<template>
  <div class="version">
    <section class="centered">
      <h3>
        <i class="far fa-check-circle icon-check d-none d-xl-block" />
        <strong>Bootstrap Studio 4.5.2</strong>
        is here! See what's new on our
        <a href="#" target="_blank">releases page »</a>
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
export default {}
</script>

<style lang="scss" scoped>
@import '~/assets/scss/_variables.scss';
@import '~/assets/scss/_sizes.scss';
@import '~/assets/scss/_mixins.scss';

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
    h3 {
      max-width: $max-width-unit * 1.11;
      @include title-left-300;

      @media (max-width: 767.98px) {
        @include text-center;
      }
      .icon-check {
        font-size: 56px;
        font-weight: 700;
        @include icon-left;
      }
    }
    .youtube {
      padding-bottom: $padding-unit * 0.75;
      height: 450px;
      @include height-media;
      .responsive-youtube {
        @include full-size;
      }
    }
  }
}

</style>
