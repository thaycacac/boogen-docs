<template>
  <div class="code">
    <h3 class="title">
      {{ title }}
    </h3>
    <p class="description">
      {{ description }}
    </p>
    <div class="retro">
      <img
        :src="require('@/assets/images/header/slider3.png')"
        alt="image"
        class="img-item"
      >
    </div>
    <b-container class="features">
      <b-row>
        <b-col md="6" sm="12" cols="12" class="item">
          <i class="far fa-folder-open icon d-none d-md-block" />
          <div class="item-detail">
            <h4 class="head">
              {{ headAdvanced }}
            </h4>
            <p class="text">
              {{ textAdvanced }}
            </p>
          </div>
        </b-col>
        <b-col md="6" sm="12" cols="12" class="item">
          <i class="far fa-folder-open icon d-none d-md-block" />
          <div class="item-detail">
            <h4 class="head">
              {{ headJS }}
            </h4>
            <p class="text">
              {{ textJS }}
            </p>
          </div>
        </b-col>
        <b-col md="6" sm="12" cols="12" class="item">
          <i class="far fa-folder-open icon d-none d-md-block" />
          <div class="item-detail">
            <h4 class="head">
              {{ headHTML }}
            </h4>
            <p class="text">
              {{ textHTML }}
            </p>
          </div>
        </b-col>
        <b-col md="6" sm="12" cols="12" class="item">
          <i class="far fa-folder-open icon d-none d-md-block" />
          <div class="item-detail">
            <h4 class="head">
              {{ headImport }}
            </h4>
            <p class="text">
              {{ textImport }}
            </p>
          </div>
        </b-col>
      </b-row>
    </b-container>
  </div>
</template>

<script>
export default {
  data() {
    return {
      title: 'Editing Code',
      description:
        'For some things drag and drop isn\'t enough. This is why Bootstrap Studio gives you full control over your markup when you need it. You can import and edit CSS, SASS, JavaScript and HTML in our Sublime Text-like editor.',
      headAdvanced: 'Advanced CSS and SASS Editors',
      headJS: 'JavaScript Editing',
      headHTML: 'HTML Editing',
      headImport: 'Import Existing Websites',
      textAdvanced:
        'Our advanced CSS editing interface supports auto suggest and rule validation, and shows the active and inherited rules at an any given time. You will soon dread having to go back to your text editor.',
      textJS:
        'Write JavaScript in our Sublime Text-like editor. All your changes are synced with the preview, so you can write code and try it out without having to reload your browser.',
      textHTML: 'With our powerful Custom Code component, you can write HTML directly, without going through our drag and drop interface. You can also convert any piece of your page into Custom Code when you need it.',
      textImport: 'If you have a website that you\'ve developed previously, you can import it. Just drag and drop the HTML, CSS, JS files and images into Bootstrap Studio and they will be added to your project.'
    }
  },
}
</script>

<style lang="scss" scoped>
@import '~/assets/scss/_variables.scss';
@import '~/assets/scss/_sizes.scss';
@import '~/assets/scss/_mixins.scss';

$size-unit: 24px;

.code {
  background-color: $color-gray-200;
  padding-top: $padding-unit;
  .title {
    @include title-700;
    @include text-center;
  }
  .description {
    @include text-muted($color-black);
    max-width: $max-width-unit;
    @media (max-width: 575.98px) {
      @include container;
    }
  }
  .retro{
    max-width: $max-width-unit;
    margin: $margin-unit * 0.5 auto;
    padding-bottom: $padding-unit * 0.5;
    .img-item{
      width: 100%;
      @media (max-width: 575.98px) {
        @include container;
      }
    }
  }
  .features {
    .item {
      padding-top: $padding-unit * 0.5;
      padding-bottom: $padding-unit * 0.5;
      .icon {
        color: $color-blue;
        float: left;
        font-size: $size-unit;
      }
      .item-detail {
        padding-left: $padding-unit * 0.75;
        .head{
          color: $color-black;
        }
      }
    }
  }
}
</style>

