<template>
  <b-container>
    <p class="title">
      Hello world!!!
    </p>
    <Header />
  </b-container>
</template>

<script>
import { Header } from '~/components'

export default {
  components: {
    Header,
  },
}
</script>

<style lang="scss" scoped>
@import '~/assets/scss/main.scss';

.title {
  color: $color-gray-700;
  @include text-center;
}
</style>
