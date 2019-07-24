<template>
  <div>
    <Header />
    <Intro />
    <Version />
    <Interface />
    <Templates />
  </div>
</template>

<script>
import { Header , Intro , Version , Interface , Templates } from '~/components'

export default {
  components: {
    Header,
    Intro,
    Version,
    Interface,
    Templates,
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
