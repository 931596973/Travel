<template>
  <div class="wapper">
    <swiper :options="swiperOption">
      <swiper-slide v-for="item of swiperList" :key="item.id">
        <img class="swiper-img" :src="item.imgUrl">
      </swiper-slide>
      <div class="swiper-pagination" slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeSwiper',
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true
      },
      swiperList: [{
        id: '0001',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1805/9c/ba7b402ad572c902.jpg_750x200_a83ca8d6.jpg'
      }, {
        id: '0002',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1809/d4/e298dff35d3af802.jpg_750x200_9b0d56c1.jpg'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  .wapper >>> .swiper-pagination-bullet-active
    background-color #fff
  .wapper
    width 100%
    overflow hidden
    height 0
    padding-bottom 31.25%
    .swiper-img
      width 100%
</style>
