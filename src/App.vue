<script>

import axios from 'axios';
import { store } from './store'

import CardComp from './components/CardComp.vue'


export default {
  name: "App",
  components: {
    CardComp
  }
}
</script>

<template>
  <CardComp />
</template>

<style lang="scss">
@use "./style/main.scss" as *;
</style>
