<template>
  <div class="purchase">
    <h3 class="title">
      {{ title }}
    </h3>
    <p class="description">
      {{ description }}
    </p>
    <div class="packages">
      <div class="package standard">
        <h4 class="head">
          {{ headStandard }}
        </h4>
        <p class="text">
          {{ textStandard }}
        </p>
        <div class="item">
          <i class="far fa-check-circle icon" />
          <h5 class="item-text">
            {{ runOn }}
          </h5>
          <span>
            <i class="far fa-question-circle ques-icon" />
          </span>
        </div>
        <div class="item">
          <i class="far fa-check-circle icon" />
          <h5 class="item-text">
            {{ install }}
          </h5>
          <span>
            <i class="far fa-question-circle ques-icon" />
          </span>
        </div>
        <div class="item">
          <i class="far fa-check-circle icon" />
          <h5 class="item-text">
            {{ buyOnce }}
          </h5>
          <span>
            <i class="far fa-question-circle ques-icon" />
          </span>
        </div>
        <div class="item">
          <i class="far fa-check-circle icon" />
          <h5 class="item-text">
            {{ freeHost }}
          </h5>
          <span>
            <i class="far fa-question-circle ques-icon" />
          </span>
        </div>
        <div class="item">
          <i class="far fa-check-circle icon" />
          <h5 class="item-text">
            {{ freeUpgrade }}
          </h5>
          <span>
            <i class="far fa-question-circle ques-icon" />
          </span>
        </div>
        <h4 class="price centered">
          {{ priceStandard }}
        </h4>
        <div class="centered">
          <b-button pill variant="primary btn-lg">
            {{ btnPurchase }}
          </b-button>
        </div>
        <div class="special-offer centered">
          <span class="limited">{{ limited }}</span>
          <p>{{ offer }}</p>
        </div>
      </div>
      <div class="package life-time">
        <h4 class="head">
          {{ headLifetime }}
        </h4>
        <p class="text">
          {{ textLifetime }}
        </p>
        <div class="item">
          <i class="far fa-check-circle icon" />
          <h5 class="item-text">
            {{ fullStandard }}
          </h5>
        </div>
        <div class="item">
          <i class="far fa-check-circle icon" />
          <h5 class="item-text">
            {{ upgForever }}
          </h5>
        </div>
        <h4 class="price centered">
          {{ priceLifetime }}
        </h4>
        <div class="centered">
          <b-button pill variant="info btn-lg">
            {{ btnLifeTime }}
          </b-button>
        </div>
        <div class="special-offer centered">
          <span class="limited">{{ limited }}</span>
          <p>{{ offer }}</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      priceStandard: '$29',
      priceLifetime: '$60',
      title: 'Purchase',
      description:
        'Bootstrap Studio is a desktop application that works fully offline. There are no monthly payments, usage limits or ongoing fees. You buy it once and own it forever.',
      headStandard: 'Standard',
      headLifetime: 'Lifetime',
      textStandard:
        'Bootstrap Studio Standard is the perfect tool for developers, designers and individuals with interest in web development.',
      textLifetime:
        "Bootstrap Studio Lifetime is a special version of our app. It has all powerful features and you'll receive every new version for free, forever.",
      runOn: 'Runs on Win 7+, macOS, Linux',
      install: 'Install it on all your computers',
      buyOnce: 'Buy it once, own it forever',
      freeHost: 'Free Web Hosting and Forms',
      freeUpgrade: '1 year of free upgrades',
      btnPurchase: 'Buy Standard',
      btnLifeTime: 'Buy LifeTime',
      limited: 'limited time',
      offer: 'Buy today and get our premium templates for free!',
      fullStandard: 'Everything from Standard',
      upgForever: 'Free upgrades forever!',
    }
  },
}
</script>

<style lang="scss" scoped>
@import '~/assets/scss/_variables.scss';
@import '~/assets/scss/_sizes.scss';
@import '~/assets/scss/_mixins.scss';
$font-unit: 20px;
$small-unit: 3px;
$font-weight-unit: 400;
$zero-unit: 0;

.purchase {
  padding-top: $padding-unit * 2;
  .title {
    @include title-700;
    @include text-center;
    padding-bottom: $padding-unit;
  }
  .description {
    @include text-muted($color-black);
    max-width: $max-width-unit;
    @media (max-width: 575.98px) {
      @include container;
    }
  }
  .packages {
    display: flex;
    justify-content: center;
    align-items: center;
    max-width: $max-width-unit * 1.57;
    margin: 0px auto;
    @media (max-width: 767.98px) {
      display: block;
    }
    .package {
      padding: $padding-unit $padding-unit;
      @include box-shadow;
      border-radius: $small-unit * 3;
      background: $color-white;
      width: 50%;
      @media (max-width: 767.98px) {
        width: 100%;
      }
    }
    .standard {
      .text {
        @include text-muted($color-black);
        padding-top: $padding-unit;
      }
      .item {
        @include item-package();
        .item-text {
          font-size: $unit;
        }
        .icon {
          @include icon-check-package($color-blue);
        }
        .ques-icon {
          position: absolute;
          top: $zero-unit;
          right: $zero-unit;
          margin-top: $small-unit;
          color: $color-blue-200;
        }
      }
    }
    .life-time {
      border-top-left-radius: $zero-unit;
      border-bottom-left-radius: $zero-unit;
      background-color: $color-blue;
      color: $color-white;
      .text {
        @include text-muted($color-white);
        padding-top: $padding-unit;
      }
      .item {
        @include item-package();
        .item-text {
          font-size: $unit;
        }
        .icon {
          @include icon-check-package($color-white);
        }
      }
    }
  }
}

.btn-lg {
  @include btn-lg;
  @include box-shadow;
}
.centered {
  @include text-center;
}
.price {
  @include price-package;
}
.head {
  @include package-head();
}
.special-offer {
  @include border-area($color-gray-400);
}
.limited {
  @include limit-span;
}
</style>

