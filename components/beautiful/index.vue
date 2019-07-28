<template>
  <div class="beautiful">
    <h3 class="title">
      {{ title }}
    </h3>
    <p class="description">
      {{ description }}
    </p>
    <b-container class="features">
      <b-row>
        <b-col md="6" sm="12" cols="12" class="item">
          <i class="fas fa-directions icon d-none d-md-block" />
          <div class="item-detail">
            <h4 class="head">
              {{ head_1 }}
            </h4>
            <p class="text">
              {{ text_1 }}
            </p>
          </div>
        </b-col>
        <b-col md="6" sm="12" cols="12" class="item">
          <i class="fas fa-asterisk icon d-none d-md-block" />
          <div class="item-detail">
            <h4 class="head">
              {{ head_2 }}
            </h4>
            <p class="text">
              {{ text_2 }}
            </p>
          </div>
        </b-col>
        <b-col md="6" sm="12" cols="12" class="item">
          <i class="fas fa-link icon d-none d-md-block" />
          <div class="item-detail">
            <h4 class="head">
              {{ head_1 }}
            </h4>
            <p class="text">
              {{ text_1 }}
            </p>
          </div>
        </b-col>
        <b-col md="6" sm="12" cols="12" class="item">
          <i class="fas fa-folder icon d-none d-md-block" />
          <div class="item-detail">
            <h4 class="head">
              {{ head_2 }}
            </h4>
            <p class="text">
              {{ text_2 }}
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
      title: 'Beautiful Components',
      description:
        'Bootstrap Studio comes with a large number of pretty components for building responsive pages. We  slideshows and even basic elements like spans and divs. See some of them below.',
      head_1: 'Smart Drag & Drop',
      head_2: 'Create Your Own Components',
      text_1:
        'Bootstrap Studio knows which Bootstrap components can be nested in one another and gives you suggestions. It automatically generates beautiful HTML for you, which looks as if it was written by hand by an expert.',
      text_2:
        'You can extract pieces of your designs as Custom Components, and have them ready to be dropped into any design you create. You can also export these components as files and share them.',
    }
  },
}
</script>

<style lang="scss" scoped>
@import '~/assets/scss/_variables.scss';
@import '~/assets/scss/_sizes.scss';
@import '~/assets/scss/_mixins.scss';

$size-unit: 24px;

.beautiful {
  background-color: $color-gray-200;
  padding-top: $padding-unit;
  .title {
    @include title-700;
    @include text-center;
  }
  .description {
    @include text-muted($color-black);
    max-width: $max-width-unit;
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

