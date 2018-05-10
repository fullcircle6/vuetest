<template>
  <div class="home">
      <home-header></home-header>
      <home-swiper></home-swiper>
      <home-icons></home-icons>
      <!-- <home-hotsale></home-hotsale> -->
      <home-recommend></home-recommend>
      <home-weekend></home-weekend>
  </div>
</template>

<script>
import HomeHeader from './components/Header'
import HomeSwiper from './components/Swiper'
import HomeIcons from './components/Icons'
// import HomeHotsale from './components/HotSale'
import HomeRecommend from './components/Recommend'
import HomeWeekend from './components/Weekend'
export default {
  name: 'Home',
  components: {
    HomeHeader,
    HomeSwiper,
    HomeIcons,
    // HomeHotsale,
    HomeRecommend,
    HomeWeekend
  }
}
</script>
<style lang="stylus" scoped>
</style>
