<template>
  <div :class="$style.main">
    <HeaderMain />
    <div :class="$style.max_size">
      <Sofa />
      <Slider />
    </div>
    <GetStart />
    <Footer />
  </div>
</template>

<script>
import HeaderMain from '@/components/HeaderMain/HederMain.vue'
import Sofa from '@/components/Sofa/Sofa.vue'
import Slider from '@/components/Slider/Slider.vue'
import GetStart from '@/components/GetStart/GetStart.vue'
import Footer from '@/components/Footer/Footer.vue'
export default {
  components: {
    HeaderMain,
    Sofa,
    Slider,
    GetStart,
    Footer,
  },
}
</script>

<style lang="scss" module>
.main {
  margin: 0 auto;
}

.max_size {
  max-width: 1230px;
  margin: 0 auto;
}
</style>
