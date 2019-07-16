<template>
  <div class="header">
    <div class="row">
      <div class="col-lg-6 col-md-6 col-sm-6">
        <div class="illustration">
          <img src="~/static/app_4.jpg" class="img-responsive" alt>
        </div>
      </div>
      <div class="col-md-6 col-md-6 col-sm-6">
        <h1>Bootstrap Studio</h1>
        <p class="text-muted">
          A powerful desktop app for creating
          <strong>responsive websites</strong>
          using the
          <strong>Bootstrap framework.</strong>
        </p>
        <button id="run-browser-demo" class="btn btn-primary">
          Run Browser Demo
        </button>
      </div>
    </div>
    <a href="#intro">
      <span class="btn-scroll" />
    </a>
  </div>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
@import '~/assets/scss/main.scss';

.header {
  background-color: $color-gray-900;
  padding: 65px 60px 60px;
  min-height: 32rem;
  position: relative;
  .row {
    display: flex;
    align-items: center;
    flex-grow: 1;
  }
  .illustration {
    transform: perspective(2000px) rotateY(36deg) scale(1.25) translateX(40px);
    max-width: 700px;
    margin-left: auto;
    .img-responsive {
      width: 100%;
    }
  }
  .illustration::after {
    content: '';
    position: absolute;
    width: 100%;
    height: 100%;
    top: 0;
    left: 0;
    background: linear-gradient(to right, #0c161f00 49%, #0c161f);
    z-index: 10;
    pointer-events: none;
  }
  h1 {
    font-weight: 700;
    font-size: 48px;
    color: $color-white;
  }
  .text-muted {
    font-size: 24px;
    font-weight: 400;
    strong {
      color: $color-white;
    }
  }
  #run-browser-demo {
    border-radius: 2rem;
    padding: 0.9em 1.2em 1em;
    line-height: 1;
    font-weight: 700;
  }
  .btn-scroll {
    position: absolute;
    bottom: 40px;
    left: 50%;
    width: 44px;
    margin-left: -22px;
    height: 44px;
    border-radius: 50%;
    border: 1px solid #fff;
    animation: sdb 2s infinite;
    z-index: 1;
    opacity: 0.6;
  }
  @-webkit-keyframes sdb {
    0%,
    40% {
      -webkit-transform: translate(0, 0);
      transform: translate(0, 0);
    }
    20% {
      -webkit-transform: translateY(10px);
      transform: translateY(10px);
    }
  }
  .btn-scroll::before {
    content: '';
    top: 11px;
    left: 14px;
    width: 14px;
    height: 14px;
    border-left: 1px solid #fff;
    border-bottom: 1px solid #fff;
    transform: rotate(-45deg);
    position: absolute;
  }
}
</style>

