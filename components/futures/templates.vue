<template>
  <div class="templates">
    <h3>
      {{ title }}
    </h3>
    <p>
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
  h3 {
    @include title-700;
    @include text-center;
  }
  p {
    @include text-muted(#fff);
    max-width: $max-width-unit;
    @media (max-width: 575.98px) {
      padding-top: $padding-unit;
      @include container;
    }
  }
}
</style>

