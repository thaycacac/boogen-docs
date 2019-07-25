<template>
  <div id="intro" class="container">
    <section class="centered intro">
      <h1 class="text-center title">
        {{ title }}
      </h1>
      <p class="description">
        {{ description }}
      </p>
    </section>
  </div>
</template>

<script>
export default {
  data() {
    return {
      title: 'Boogen is a powerful desktop app for designing and prototyping websites.',
      description:
        'It comes with a large number of built-in components, which you can drag and drop to assemble responsive web pages. The app is built on top of the hugely popular Bootstrap framework, and exports clean and semantic HTML.',
    }
  },
}
</script>

<style lang="scss" scoped>
@import '~/assets/scss/_variables.scss';
@import '~/assets/scss/_sizes.scss';
@import '~/assets/scss/_mixins.scss';

.centered {
  max-width: $max-width-unit * 1.33;
  text-align: center;
}
section {
  margin: $margin-unit * 2 auto;
  @media (max-width: 575.98px) {
    margin: $margin-unit * 1.25 auto;
  }
  .title {
    max-width: $max-width-unit;
    margin: 0 auto $margin-unit * 1.25;
    @include title-700;

    @media (max-width: 575.98px) {
      line-height: 1.3;
      font-size: $unit * 1.75;
    }
  }
  .description {
    @include text-muted(#59697d);
  }
}
</style>

