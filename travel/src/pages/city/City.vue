<template>
<div>
  <city-header></city-header>
  <city-search></city-search>
  <city-list :cities="cities" :hot="hotCities"></city-list>
  <city-alphabet :cities="cities"></city-alphabet>
</div>
</template>

<script>
import CityHeader from './compoents/Header.vue'
import CitySearch from './compoents/Search.vue'
import CityList from './compoents/List.vue'
import CityAlphabet from './compoents/alphabet.vue'
import axios from 'axios'
export default {
  name: 'City',
  components: {
    CityHeader,
    CitySearch,
    CityList,
    CityAlphabet
  },
  data () {
    return {
      cities: {},
      hotCities: []
    }
  },
  mounted () {
    this.getCityInfo()
  },
  methods: {
    getCityInfo () {
      axios.get('/api/city.json')
        .then(this.handalGetCityInfoSucc)
    },
    handalGetCityInfoSucc (res) {
      res = res.data
      if (res.ret && res.data) {
        const data = res.data
        this.cities = data.cities
        this.hotCities = data.hotCities
      }
    }
  }
}
</script>

<style lang="stylus" scoped>

</style>
