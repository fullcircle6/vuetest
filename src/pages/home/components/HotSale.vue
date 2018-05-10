<template>
  <div class='hotsale_wrapper'>
      <div class="hotsale-grouptitle">
        <img class="hotsale-title-img"  src="http://img1.qunarzz.com/piao/fusion/1711/16/bfbb9874e8f11402.png" alt="本周热门榜单">
        <span class="hotsale-title">本周热门榜单</span>
        <a class="hotsale-title-more" href="http://touch.piao.qunar.com/touch/weekHotSales.htm?cityName=北京">全部榜单
        <span class="hotsale-iconfont hotsale-more-icon">F</span>
        </a>
      </div>
  </div>
</template>
<script>
export default {
  name: 'HotSale',
  data () {
    return {
    }
  }
}
</script>
<style lang="stylus" scoped>
  .hotsale_wrapper
    margin-top: .3rem
    width:100%
    overflow: hidden
    padding-bottom:50%
    background:#fff
    padding-top: .2rem
    .hotsale-title-img
      display: inline-block
      overflow: hidden
      width:.4rem
      height: .4rem
      margin-left: .2rem
      vertical-align: top 
    .hotsale-title
      display: inline-block
      margin-left: .08rem
      height: .44rem
      color: #212121
      font-size: .32rem
      line-height: .44rem
    .hotsale-title-more
      display: inline-block
      float: right
      margin-right: .32rem
      color: #616161
      font-size: .24rem
      line-height: .28rem
      margin-top: .09rem
</style>
