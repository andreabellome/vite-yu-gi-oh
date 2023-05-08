<script>
import HeaderComponent from './components/HeaderComponent.vue'
import FooterComponent from './components/FooterComponent.vue'
import MainComponent from './components/MainComponent.vue'

export default {
  name: "App",
  components: {
    HeaderComponent,
    MainComponent,
    FooterComponent
  }
}
</script>

<template>
  cciao
  <div>
    <HeaderComponent />

    <MainComponent />

    <FooterComponent />
  </div>
</template>

<style lang="scss">
@use "./style/main.scss" as *;
</style>
