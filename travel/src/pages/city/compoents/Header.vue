<template>
<div class="header">
  城市选择
  <router-link to="/">
    <div class="iconfont header-back">&#xe624;</div>
  </router-link>
</div>
</template>

<script>
export default {
  name: 'City'
}
</script>

<style lang="stylus" scoped>
@import '~styles/varibles.styl'
  .header
    position relative
    overflow hidden
    height $headerColor
    line-height $headerColor
    text-align center
    color #fff
    background $bgColor
    font-size .32rem
    border none
    .header-back
      top 0
      left 0
      position absolute
      width .64rem
      text-align center
      font-size .4rem
      color #fff
</style>
