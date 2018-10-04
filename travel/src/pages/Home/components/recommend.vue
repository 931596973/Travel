<template>
<div>
  <div class="recomment-title">热销推荐</div>
  <ul>
    <li class="item border-bottom" v-for="item of list" :key="item.id">
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
  props: {
    list: Array
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
