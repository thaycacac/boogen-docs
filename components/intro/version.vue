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
@import '~/assets/scss/main.scss';

.version {
  background-color: #f4f8fb;
  section {
    padding-top: 60px;
    text-align: center;
    max-width: 800px;
    margin: 0 auto;
    h3 {
      max-width: 480px;
      margin: 0 auto 50px;
      line-height: 1.45;
      font-size: 25px;
      text-align: left;
      font-weight: 300;
      .icon-check {
        font-size: 56px;
        font-weight: 700;
        color: #2789e4;
        float: left;
        margin-top: 9px;
        margin-right: 22px;
      }
    }
    .youtube {
      padding-bottom: 30px;
      height: 450px;
      .responsive-youtube {
        width: 100%;
        height: 100%;
      }
    }
  }
}
@media (max-width: 575.98px) {
  .version {
    padding-left: 15px;
    padding-right: 15px;
    section {
       padding-top: 40px;
      h3 {
        text-align: center;
      }
      .youtube {
        height: 230px !important;
      }
    }
  }
}
@media (min-width: 576px) and (max-width: 767.98px) {
  .version {
    padding-left: 15px;
    padding-right: 15px;
    section {
      padding-top: 30px;
      h3 {
        text-align: center;
      }
      .youtube {
        height: 350px !important;
      }
    }
  }
}
</style>
