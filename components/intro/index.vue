<template>
  <div id="intro" class="container">
    <section class="centered intro">
      <h1 class="text-center">
        <strong>Bootstrap Studio</strong>
        is a powerful desktop app for designing and prototyping websites.
      </h1>
      <p>It comes with a large number of built-in components, which you can drag and drop to assemble responsive web pages. The app is built on top of the hugely popular Bootstrap framework, and exports clean and semantic HTML.</p>
    </section>
  </div>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
@import '~/assets/scss/main.scss';
.centered {
  max-width: 800px;
  text-align: center;
}
section {
  margin: 80px auto;
  h1 {
    max-width: 620px;
    margin: 0 auto 50px;
    line-height: 1.5;
    font-size: 32px;
    font-weight: 300;
  }
  p {
    font-size: 20px;
    line-height: 1.45;
    max-width: 680px;
    margin: 0 auto 50px;
    color: #50595f;
  }
}
@media (max-width: 575.98px){
  section {
    margin: 50px auto;
    h1 {
    line-height: 1.3;
    font-size: 28px;
  }
  }
}
</style>
