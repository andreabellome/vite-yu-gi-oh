<script>

import axios from 'axios';
import { store } from './store'

import HeaderComp from './components/HeaderComp.vue'
import CardComp from './components/CardComp.vue'


export default {
  name: "App",
  components: {
    CardComp,
    HeaderComp
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
