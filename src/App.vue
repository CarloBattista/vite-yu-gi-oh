<script>
import axios from "axios";
import {store} from "./store"
import HeaderComp from "./components/HeaderComp.vue"
import TypeSelector from "./components/TypeSelector.vue"
import MainComp from "./components/MainComp.vue"

export default {
  name: "App",
  components: {
    HeaderComp,
    TypeSelector,
    MainComp,
  },
  data(){
    return{
      store
    }
  },
  mounted() {
    axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php?num=20&offset=0')
      .then((res) => {
      store.arrayCards = res.data.data
        // console.log(res.data.data)
      })
  },
}
</script>

<template>
  <HeaderComp />
  <TypeSelector />
  <MainComp />
</template>

<style lang="scss">
@use "./styles/main.scss" as *;
</style>
