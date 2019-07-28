<template>
  <div>
    <Header />
    <Intro />
    <Version />
    <Interface />
    <Templates />
    <Beautiful />
    <Realtime />
    <EditCode />
  </div>
</template>

<script>
import { Header , Intro , Version , Interface , Templates, Beautiful, Realtime, EditCode } from '~/components'

export default {
  components: {
    Header,
    Intro,
    Version,
    Interface,
    Templates,
    Beautiful,
    Realtime,
    EditCode,
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
