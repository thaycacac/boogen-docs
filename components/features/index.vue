<template>
  <div class="features d-none d-md-block">
    <div class="code">
      <h3 class="title">
        {{ title }}
      </h3>
      <p class="description">
        {{ description }}
      </p>
      <b-container class="list-features">
        <b-row>
          <b-col md="6" sm="12" cols="12" class="item">
            <i class="far fa-heart icon d-none d-md-block" />
            <div class="item-detail">
              <h4 class="head">
                {{ headBuilt }}
              </h4>
              <p class="text">
                {{ textBuilt }}
              </p>
            </div>
          </b-col>
          <b-col md="6" sm="12" cols="12" class="item">
            <i class="far fa-paper-plane icon d-none d-md-block" />
            <div class="item-detail">
              <h4 class="head">
                {{ headPublish }}
              </h4>
              <p class="text">
                {{ textPublish }}
              </p>
            </div>
          </b-col>
          <b-col md="6" sm="12" cols="12" class="item">
            <i class="far fa-square icon d-none d-md-block" />
            <div class="item-detail">
              <h4 class="head">
                {{ headGrid }}
              </h4>
              <p class="text">
                {{ textGrid }}
              </p>
            </div>
          </b-col>
          <b-col md="6" sm="12" cols="12" class="item">
            <i class="fas fa-radiation icon d-none d-md-block" />
            <div class="item-detail">
              <h4 class="head">
                {{ headSmooth }}
              </h4>
              <p class="text">
                {{ textSmooth }}
              </p>
            </div>
          </b-col>
          <b-col md="6" sm="12" cols="12" class="item">
            <i class="far fa-sticky-note icon d-none d-md-block" />
            <div class="item-detail">
              <h4 class="head">
                {{ headGG }}
              </h4>
              <p class="text">
                {{ textGG }}
              </p>
            </div>
          </b-col>
          <b-col md="6" sm="12" cols="12" class="item">
            <i class="fas fa-bolt icon d-none d-md-block" />
            <div class="item-detail">
              <h4 class="head">
                {{ headProd }}
              </h4>
              <p class="text">
                {{ textProd }}
              </p>
            </div>
          </b-col>
          <b-col md="6" sm="12" cols="12" class="item">
            <i class="far fa-image icon d-none d-md-block" />
            <div class="item-detail">
              <h4 class="head">
                {{ headThemes }}
              </h4>
              <p class="text">
                {{ textThemes }}
              </p>
            </div>
          </b-col>
          <b-col md="6" sm="12" cols="12" class="item">
            <i class="fas fa-cloud-upload-alt icon d-none d-md-block" />
            <div class="item-detail">
              <h4 class="head">
                {{ headUpToDate }}
              </h4>
              <p class="text">
                {{ textUpToDate }}
              </p>
            </div>
          </b-col>
        </b-row>
      </b-container>
      <div class="try-browser">
        <b-row>
          <b-col md="6">
            <img 
              :src="require('@/assets/images/home/Google_Chrome_logo.png')"
              alt="logo bootstrap"
              width="150"
              class="img-chrome"
            >
          </b-col>
          <b-col md="6">
            <h3 class="head">
              {{ titleBrowser }}
            </h3>
            <p class="sub-head">
              {{ descriptionBrowser }}
            </p>
          </b-col>
        </b-row>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      title: 'Even More Features',
      titleBrowser: 'Try it in your browser',
      descriptionBrowser:
        'We have an interactive demo of Bootstrap Studio that runs in Google Chrome. No installation required!',
      description:
        'Bootstrap Studio is a revolutionary website builder. With its productivity features and specialized Bootstrap tools, you can create everything from a prototype to a fully working website.',

      headBuilt: 'Built for Bootstrap 3 and 4',
      headPublish: 'One-click Publishing',
      headGrid: 'Grid Tools',
      headSmooth: 'Smooth Animations',
      headGG: 'Google Webfonts',
      headProd: 'Productivity Features',
      headThemes: 'Themes and Icons',
      headUpToDate: 'Always Up to Date',

      textBuilt:
        'Bootstrap Studio knows how to construct a valid Bootstrap page and automatically writes the correct HTML. It supports both Bootstrap 3 and Bootstrap 4 and you can convert your designs from one to the other.',
      textPublish:
        'You can export your design as a static website, or publish it with one click to our next gen hosting platform. It offers HTTPS, custom domains, passkeys and is totally free!',
      textGrid:
        'The app has specialized tools for working with the Bootstrap grid. Easily create, resize and offset columns, and apply responsive visibility classes.',
      textSmooth:
        'In our app, you can create smooth CSS animations that are triggered on browser scroll or hover. We also have a special Parallax component for beautiful image backgrounds.',
      textGG:
        'Bootstrap Studio is integrated with Google Webfonts and gives you an easy way to import and manage your fonts. Font family names are even auto-suggested in our css editor.',
      textProd:
        'Bootstrap Studio has comprehensive support for keyboard shortcuts which allow you to speed up your workflow dramatically.',
      textThemes:
        'The app has a number of built-in Bootstrap themes, icon fonts, templates and components, which you can combine into beautiful and unique designs.',
      textUpToDate:
        'Bootstrap Studio updates automatically, so you always have the latest version. We release updates every month, filled with new features, components and improvements.',
    }
  },
}
</script>

<style lang="scss" scoped>
@import '~/assets/scss/_variables.scss';
@import '~/assets/scss/_sizes.scss';
@import '~/assets/scss/_mixins.scss';

$size-unit: 24px;

.features {
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
  .list-features {
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
        .head {
          color: $color-black;
        }
      }
    }
  }
  .try-browser {
    background-color: $color-blue;
    padding-bottom: $padding-unit * 0.5;
    .head {
      @include title-700;
      color: $color-white;
      padding-top: $padding-unit;
    }
    .sub-head {
      color: $color-white;
      max-width: $max-width-unit;
      @media (max-width: 575.98px) {
        @include container;
      }
    }
    .img-chrome{
      float: right;
      padding-top: $padding-unit * 0.5;
    }
  }
}
</style>
