<template>
    <div class="header">
        <div class="header-left">
          <div class="iconfont back-icon">&#xe624;</div>
        </div>
        <div class="header-input">
          <span class="iconfont">&#xe632;</span>
          输入城市/景点/游玩主题
          </div>
        <router-link to="/city">
          <div class="header-right">
            {{this.city}}
            <span class="iconfont arrow-icon">&#xe64a;</span>
          </div>
        </router-link>
    </div>
</template>
<script>
export default {
  name: 'HomeHeader',
  props: {
    city: String
  }
}
</script>
<style lang="stylus" scoped>
@import '~styles/varibles.styl'
  .header
    display flex
    line-height: .86rem
    background $bgColor
    color #fff
    .header-left
      width .64rem
      float left
      .back-icon
        display block
        text-align center
    .header-right
      width 1.24rem
      float right
      text-align center
      color #fff
      .arrow-icon
        margin-left -.04rem
        font-size .24rem
    .header-input
      padding-left .2rem
      flex 1
      color #ccc
      margin-top .12rem
      margin-left .2rem
      border-radius .1rem
      background #fff
      height .64rem
      line-height .64rem
</style>
