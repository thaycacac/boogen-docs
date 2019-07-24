<template>
  <div class="templates">
    <h3>Beautiful Templates</h3>
    <p>The app comes with a number of premium, fully responsive templates that you can customize. Each template consists of multiple pages and widgets you can pick-and-match into the perfect website.</p>
    <div class="swiper-container">
      <!-- Additional required wrapper -->
      <div class="swiper-wrapper">
        <!-- Slides -->
        <div class="swiper-slide">
          Slide 1
        </div>
        <div class="swiper-slide">
          Slide 2
        </div>
        <div class="swiper-slide">
          Slide 3
        </div>...
      </div>
      <!-- If we need pagination -->
      <div class="swiper-pagination" />

      <!-- If we need navigation buttons -->
      <div class="swiper-button-prev" />
      <div class="swiper-button-next" />

      <!-- If we need scrollbar -->
      <div class="swiper-scrollbar" />
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
@import '~/assets/scss/main.scss';
.templates {
  background-color: #3d7aef;
  color: $color-white;
  padding-top: 40px;
  h3 {
    font-weight: 700;
    text-align: center;
    font-size: 36px;
    margin-bottom: 40px;
  }
  p {
    text-align: center;
    font-size: 18px;
    line-height: 1.5;
    margin: 0 auto 50px;
    max-width: 600px;
    font-weight: 400;
  }
}
</style>

