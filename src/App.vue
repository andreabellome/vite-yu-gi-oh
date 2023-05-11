<script>

import axios from 'axios';
import { store } from './store'

import HeaderComp from './components/HeaderComp.vue'
import CardComp from './components/CardComp.vue'
import FilterCards from './components/FilterCards.vue'


export default {
  name: "App",
  data() {
    return {
      store
    }
  },
  components: {
    CardComp,
    HeaderComp,
    FilterCards
  },
  created() {
    this.callApi();
  },
  methods: {

    callApi() {

      if (store.valueArchetype !== '') {
        axios.get(`https://db.ygoprodeck.com/api/v7/cardinfo.php?archetype=${encodeURIComponent(store.valueArchetype)} `).then((res) => {
          this.store.arrayCards = res.data.data;
        })
      }
    }
  }
}
</script>

<template>
  <HeaderComp />
  <FilterCards @nomeEmit="callApi()" />
  <CardComp />
</template>

<style lang="scss">
@use "./style/main.scss" as *;
</style>
