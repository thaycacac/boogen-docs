<template>
  <div class="feedback">
    <div class="customer">
      <h3 class="title center">
        {{ title }}
      </h3>
      <b-container>
        <b-row>
          <b-col md="4" sm="12" cols="12" class="item">
            <h4 class="content">
              {{ firstFeed }}
            </h4>
            <p class="author">
              {{ firstAuthor }}
            </p>
          </b-col>
          <b-col md="4" sm="12" cols="12" class="item">
            <h4 class="content">
              {{ secondFeed }}
            </h4>
            <p class="author">
              {{ secondAuthor }}
            </p>
          </b-col>
          <b-col md="4" sm="12" cols="12" class="item">
            <h4 class="content">
              {{ thirdFeed }}
            </h4>
            <p class="author">
              {{ thirdAuthor }}
            </p>
          </b-col>
        </b-row>
      </b-container>
    </div>
    <b-container class="subscribe">
      <h3 class="sub-title center">
        {{ subTitle }}
      </h3>
      <p class="text">
        {{ subscrible }}
      </p>
      <div class="send-info">
        <b-row>
          <b-col class="info">
            <b-form-input placeholder="Your email" class="text-input" />
          </b-col>
          <b-col>
            <b-button variant="primary btn-send">
              {{ btnSend }}
            </b-button>
          </b-col>
        </b-row>
      </div>
    </b-container>
  </div>
</template>

<script>
export default {
  data() {
    return {
      title: 'Thousands of Happy Customers',
      firstFeed:
        'I have been using Bootstrap Studio for a few days and I absolutely love what I can do with it. I have never created a good looking and functioning website so fast. I am very happy to have bought it.',
      secondFeed:
        'In no time at all I was able to fire up the app, get a quick feel for it, and create a very modern and well received site that is so much better than what we ever had before. So thank you for creating a great product, and thanks for making me look like a genius at work today!',
      thirdFeed:
        'I must say I am blown away by Bootstrap Studio. This will be the future of designing websites and making really quick "mock-ups" on the fly. It\'s also really dope as a learning tool for designers (or actually everyone) to get the hang of Bootstrap real quick.',
      firstAuthor: 'Marcus Graetz',
      secondAuthor: 'David Jones',
      thirdAuthor: 'Peter',
      subTitle: 'More Exciting Features Are Coming!',
      subscrible:
        'We update Bootstrap Studio every couple of weeks with new features and listen to your feedback on our forums. Subscribe for our newsletter and learn when we release new versions.',
      btnSend: 'Join Newsletter'    
    }
  },
}
</script>

<style lang="scss" scoped>
@import '~/assets/scss/_variables.scss';
@import '~/assets/scss/_sizes.scss';
@import '~/assets/scss/_mixins.scss';
$font-weight-unit: 300;
$border-unit: 5px;

.feedback {
  margin-top: $margin-unit * 2;
  padding-bottom: $padding-unit * 2;
  .customer {
    background-color: $color-blue;
    padding-bottom: $padding-unit;
    .title {
      @include title-700;
      color: $color-white;
      padding-top: $padding-unit;
      padding-bottom: $padding-unit;
    }
    .content {
      font-size: $unit;
      line-height: 1.4;
      margin-bottom: $unit;
      font-weight: $font-weight-unit;
      color: $color-white;
      padding: $padding-unit * 0.6 $padding-unit * 0.75;
      background-color: $color-blue-300;
      border-radius: $border-unit;
    }
    .author {
      color: $color-white;
    }
  }
  .subscribe {
    padding-top: $padding-unit;
    .sub-title {
      @include title-700;
      color: $color-black;
      padding-top: $padding-unit;
      padding-bottom: $padding-unit;
    }
    .text {
      @include text-muted($color-black);
      max-width: $max-width-unit;
      @media (max-width: 575.98px) {
        @include container;
      }
    }
    .send-info {
      max-width: 480px;
      margin: 20px auto;
      display: block;
      .info{
        margin-right: -30px;
        .text-input{
          border-radius: 0;
        }
      }
      .btn-send{
        border-top-left-radius: 0;
        border-bottom-left-radius: 0;
        border-top-right-radius: $border-unit * 4;
        border-bottom-right-radius: $border-unit * 4;
      }
    }
  }
}
.center {
  @include text-center;
}
</style>

