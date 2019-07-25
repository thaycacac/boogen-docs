<template>
  <div class="templates">
    <h3 class="title">
      {{ title }}
    </h3>
    <p class="description">
      {{ description }}
    </p>
  </div>
</template>

<script>
export default {
  data(){
    return{
      title: 'Beautiful Templates',
      description: 'The app comes with a number of premium, fully responsive templates that you can customize. Each template consists of multiple pages and widgets you can pick-and-match into the perfect website.'
    }
  }
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
}
</style>

