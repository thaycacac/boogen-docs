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
    <Features />
    <Purchase />
    <Feedback />
    <Footer />
  </div>
</template>

<script>
import { Header , Intro , Version , Interface , Templates, Beautiful, Realtime, EditCode, Features, Purchase, Feedback, Footer } from '~/components'

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
    Features,
    Purchase,
    Feedback,
    Footer,
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
