<template>
  <div>
    <Header />
    <Intro />
    <Version />
    <Interface />
  </div>
</template>

<script>
import { Header , Intro , Version , Interface } from '~/components'




export default {
  components: {
    Header,
    Intro,
    Version,
    Interface,
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
