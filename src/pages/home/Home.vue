<template>
  <div class="home">
      <home-header :city='city'></home-header>
      <home-swiper :swiperList='swiperList'></home-swiper>
      <home-icons :icons='iconList'></home-icons>
      <!-- <home-hotsale></home-hotsale> -->
      <home-recommend :recommendList='recommendList'></home-recommend>
      <home-weekend :weekendList='weekendList'></home-weekend>
  </div>
</template>

<script>
import HomeHeader from './components/Header'
import HomeSwiper from './components/Swiper'
import HomeIcons from './components/Icons'
// import HomeHotsale from './components/HotSale'
import HomeRecommend from './components/Recommend'
import HomeWeekend from './components/Weekend'
import axios from 'axios'
export default {
  name: 'Home',
  components: {
    HomeHeader,
    HomeSwiper,
    HomeIcons,
    // HomeHotsale,
    HomeRecommend,
    HomeWeekend
  },
  data () {
    return {
      city: '',
      weekendList: [],
      recommendList: [],
      swiperList: [],
      iconList: []
    }
  },
  methods: {
    getHomeInfo () {
      axios.get('/api/index.json')
        .then(this.getHomeInfoResult)
    },
    getHomeInfoResult (res) {
      res = res.data
      if (res.ret) {
        if (res.data) {
          this.city = res.data.city
          this.weekendList = res.data.weekendList
          this.swiperList = res.data.swiperList
          this.recommendList = res.data.recommendList
          this.iconList = res.data.iconList
        }
      }
      console.log(res)
    }
  },
  mounted () {
    console.log('mounted')
    this.getHomeInfo()
  }
}
</script>
<style lang="stylus" scoped>
</style>
