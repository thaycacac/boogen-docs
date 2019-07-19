<template>
  <div class="header">
    <b-row>
      <b-col xl="6" lg="12" md="12" sm="12">
        <div class="illustration">
          <img src="~/static/app_4.jpg" class="img-responsive" alt>
        </div>
      </b-col>
      <b-col xl="6" lg="12" md="12" sm="12">
        <h1>Bootstrap Studio</h1>
        <p class="text-muted">
          A powerful desktop app for creating
          <strong>responsive websites</strong>
          using the
          <strong>Bootstrap framework.</strong>
        </p>
        <b-button variant="primary" class="run-browser-demo d-none d-xl-block">
          Run Browser Demo
        </b-button>
      </b-col>
    </b-row>
    <a href="#intro" class="d-none d-xl-block">
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
    margin-left: auto;
    .img-responsive {
      width: 100%;
    }
  }

  h1 {
    font-weight: 700;
    font-size: 48px;
    color: $color-white;
  }
  .text-muted {
    font-size: 24px;
    font-weight: 400;
    max-width: 515px;
    strong {
      color: $color-white;
    }
  }
  .run-browser-demo {
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
    animation: updown 2s infinite;
    z-index: 1;
    opacity: 0.6;
  }
}
@-webkit-keyframes updown {
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
@media (max-width: 575.98px) {
  .header {
    padding: 100px 20px 40px;
    h1 {
      font-size: 28px;
      color: $color-white;
      text-align: center;
      padding-top: 15px;
    }
    .text-muted {
      font-size: 20px;
      margin-left: auto;
      margin-right: auto;
    }
  }
}
@media (min-width: 576px) and (max-width: 767.98px) {
  .header {
    padding: 85px 20px 40px;
    h1 {
      font-size: 32px;
      color: $color-white;
      text-align: center;
      padding-top: 15px;
    }
    .text-muted {
      font-size: 20px;
      margin-left: auto;
      margin-right: auto;
    }
  }
}
@media (min-width: 768px) and (max-width: 991.98px) {
  .header {
    padding: 90px 20px 40px;
    h1{
      color: $color-white;
      text-align: center;
    }
    .text-muted {
      margin-left: auto;
      margin-right: auto;
    }
  }
}

@media (min-width: 992px) and (max-width: 1199.98px) {
  .header {
    padding: 95px 20px 40px;
    h1 {
      color: $color-white;
      text-align: center;
      font-size: 32px;
      font-weight: 700;
      margin-top: 40px;
      margin-bottom: 20px;
    }
    .text-muted {
      margin-left: auto;
      margin-right: auto;
    }
    .run-browser-demo {
      top: 0;
      margin: auto;
    }
  }
}
@media (min-width: 1024.2px) {
  .illustration {
    transform: perspective(2000px) rotateY(36deg) scale(1.25) translateX(40px);
    max-width: 700px;
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
}
</style>

