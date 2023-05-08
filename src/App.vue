<script>

import axios from 'axios';
import { store } from './store'

import HeaderComp from './components/HeaderComp.vue'
import CardComp from './components/CardComp.vue'


export default {
  name: "App",
  data() {
    return {
      store
    }
  },
  components: {
    CardComp,
    HeaderComp
  },
  created() {
    this.callApi();
  },
  methods: {
    callApi() {
      axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php?num=20&offset=0').then((res) => {
        console.log(res.data.data)
        this.store.arrayCards = res.data.data;
      })
    }
  }
}
</script>

<template>
  <HeaderComp />
  <CardComp />
</template>

<style lang="scss">
@use "./style/main.scss" as *;
</style>
