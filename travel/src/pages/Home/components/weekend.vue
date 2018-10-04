<template>
<div>
  <div class="recomment-title">周末去哪儿</div>
  <ul>
    <li class="item border-bottom" v-for="item of list" :key="item.id">
      <div class="item-img-wrapper">
        <img class="item-img" :src="item.imgUrl" alt="无法显示">
      </div>
      <div class="item-info">
        <p class="item-title">{{item.title}}</p>
        <p class="item-desc">{{item.desc}}</p>
      </div>
    </li>
  </ul>
</div>
</template>

<script>
export default {
  name: 'HomeWeekend',
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
  .item-img-wrapper
    overflow hidden
    height 0
    padding-bottom 37.09%
  .item-img
    width 100%
  .item-info
    padding .1rem
    min-width 0
    .item-title
      line-height .54rem
      font-size .3rem
      ellipsis()
    .item-desc
      line-height .4rem
      font-size .25rem
      color #ccc
      ellipsis()
</style>
