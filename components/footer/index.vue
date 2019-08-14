<template>
  <div class="footer">
    <h3 class="title">
      {{ title }}
    </h3>
    <ul class="list-inline">
      <li>
        <b-link href="#">
          {{ forums }}
        </b-link>
      </li>
      <li>
        <b-link href="#">
          {{ tutorials }}
        </b-link>
      </li>
      <li>
        <b-link href="#">
          {{ license }}
        </b-link>
      </li>
      <li>
        <b-link href="#">
          {{ terms }}
        </b-link>
      </li>
      <li>
        <b-link href="#">
          {{ privacy }}
        </b-link>
      </li>
      <li>
        <b-link href="#">
          {{ bugReport }}
        </b-link>
      </li>
      <li>
        <b-link href="#">
          {{ faq }}
        </b-link>
      </li>
      <li>
        <b-link href="#">
          {{ contactUs }}
        </b-link>
      </li>
    </ul>
    <p class="copy-right">
      {{ copyRight }}
    </p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      title: 'The Revolutionary Web Design Tool.',
      forums: 'Forums',
      tutorials: 'Tutorials',
      license: 'License',
      terms: 'Terms',
      privacy: 'Privacy',
      bugReport: 'Bug Report',
      faq: 'FAQ',
      contactUs: 'Contact Us',
      copyRight: 'Copyright © 2019 Sharp Team. All Rights Reserved.'
    }
  },
}
</script>

<style lang="scss" scoped>
@import '~/assets/scss/_variables.scss';
@import '~/assets/scss/_sizes.scss';
@import '~/assets/scss/_mixins.scss';


  .footer{
    padding-top: $padding-unit;
    border-top: 1px solid $color-gray-400;
    .title{
      @include title-700;
      color: $color-gray-500;
      font-size: $unit * 1.5;
      text-align: center;
      padding-bottom: $unit;
    }
    .list-inline{
      text-align: center;
      padding-top: $unit;
      li{
        display: inline-block;
        padding-right: $unit * 0.5;
        padding-left: $unit * 0.5;
      }
    }
    .copy-right{
      text-align: center;
      padding-top: $padding-unit;
      padding-bottom: $padding-unit;
    }
  }
</style>

