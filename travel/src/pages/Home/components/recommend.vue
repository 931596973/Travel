<template>
<div>
  <div class="recomment-title">热销推荐</div>
  <ul>
    <li class="item border-bottom" v-for="item of recomendList" :key="item.id">
      <img class="item-img" :src="item.imgUrl" alt="无法显示">
      <div class="item-info">
        <p class="item-title">{{item.title}}</p>
        <p class="item-desc">{{item.desc}}</p>
        <button class="item-button">查看详情</button>
      </div>
    </li>
  </ul>
</div>
</template>

<script>
export default {
  name: 'HomeReCommend',
  data () {
    return {
      recomendList: [ {
        id: '0001',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1507/36/ce3d2d6c9ab44d67ae68d940b8781829.water.jpg_200x200_0938a8f2.jpg',
        title: '北京野生动物园',
        desc: '北京野生动物园集动物保护、野生动物驯养繁殖及科普教育为一体.'
      }, {
        id: '0002',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1507/36/ce3d2d6c9ab44d67ae68d940b8781829.water.jpg_200x200_0938a8f2.jpg',
        title: '北京野生动物园',
        desc: '北京野生动物园集动物保护、野生动物驯养繁殖及科普教育为一体.'
      }, {
        id: '0003',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1507/36/ce3d2d6c9ab44d67ae68d940b8781829.water.jpg_200x200_0938a8f2.jpg',
        title: '北京野生动物园',
        desc: '北京野生动物园集动物保护、野生动物驯养繁殖及科普教育为一体.'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
 @import '~styles/mixins.styl'
  .recomment-title
    background #eeeeee
    line-height .6rem
    text-indent .2rem
  .border-bottom
    border-bottom .01rem
    border-bottom-style solid
    border-bottom-color #eee
  .item
    display flex
    height 1.9rem
    overflow hidden
    .item-img
      width 1.7rem
      height 1.7rem
      padding .1rem
    .item-info
      flex 1
      padding .1rem
      min-width 0
      .item-title
        line-height .54rem
        font-size .32rem
        ellipsis()
      .item-desc
        line-height .4rem
        color #ccc
        ellipsis()
      .item-button
        line-height .3rem
        margin-top .2rem
        color #fff
        background #ff9300
        border-radius .06rem
        font-size .2rem
        letter-spacing .05rem
</style>
