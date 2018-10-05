<template>
<div>
  <city-header></city-header>
  <city-search></city-search>
  <city-list></city-list>
  <city-alphabet></city-alphabet>
</div>
</template>

<script>
import CityHeader from './compoents/Header.vue'
import CitySearch from './compoents/Search.vue'
import CityList from './compoents/List.vue'
import CityAlphabet from './compoents/alphabet.vue'
export default {
  name: 'City',
  components: {
    CityHeader,
    CitySearch,
    CityList,
    CityAlphabet
  }
}
</script>

<style lang="stylus" scoped>

</style>
