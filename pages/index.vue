<template>
  <div>
    <Header />
  </div>
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
@import '~/assets/scss/_variables.scss';
@import '~/assets/scss/_mixins.scss';

.title {
  color: $color-gray-700;
  @include text-center;
}
</style>
