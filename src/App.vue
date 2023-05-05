<script>
import HeaderComp from "./components/HeaderComp.vue"
import TypeSelector from "./components/TypeSelector.vue"
import MainComp from "./components/MainComp.vue"

export default {
  name: "App",
  components: {
    HeaderComp,
    TypeSelector,
    MainComp,
  }
}
</script>

<template>
  <HeaderComp/>
  <TypeSelector/>
  <MainComp/>
</template>

<style lang="scss">
@use "./styles/main.scss" as *;
</style>
