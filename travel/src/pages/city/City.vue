<template>
<div>
  <city-header></city-header>
  <city-search></city-search>
</div>
</template>

<script>
import CityHeader from './compoents/Header.vue'
import CitySearch from './compoents/Search.vue'
export default {
  name: 'City',
  components: {
    CityHeader,
    CitySearch
  }
}
</script>

<style lang="stylus" scoped>

</style>
