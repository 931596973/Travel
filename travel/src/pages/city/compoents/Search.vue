<template>
  <div class="search">
    <input type="text" class="search--input" placeholder="输入城市名或拼音">
  </div>
</template>

<script>
export default {
  name: 'CitySearch'
}
</script>

<style lang="stylus" scoped>
@import '~styles/varibles.styl'
  .search
    height .72rem
    background $bgColor
    padding 0 .1rem
    border none
    .search--input
      box-sizing border-box
      padding 0 .1rem
      line-height .62rem
      height .62rem
      width 100%
      text-align center
      border-radius .06rem
      color #666
</style>
