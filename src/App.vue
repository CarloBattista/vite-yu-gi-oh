<script>
import HeaderComp from "./components/HeaderComp.vue"
import TypeSelector from "./components/TypeSelector.vue"

export default {
  name: "App",
  components: {
    HeaderComp,
    TypeSelector,
  }
}
</script>

<template>
  <HeaderComp/>
  <TypeSelector/>
</template>

<style lang="scss">
@use "./styles/main.scss" as *;
</style>
