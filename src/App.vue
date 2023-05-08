<script>
import axios from "axios";
import { store } from "./store"
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
  data() {
    return {
      store
    }
  },
  created() {
    this.cardsApi
    this.archetypeApi
  },
  computed: {
    cardsApi() {
      if (this.store.nomeArchetype == '') {
        axios.get(`https://db.ygoprodeck.com/api/v7/cardinfo.php?num=20&offset=54`)
          .then((res) => {
            this.store.arrayCards = res.data.data
            // console.log(res.data.data)
          })
      } else {
        axios.get(` https://db.ygoprodeck.com/api/v7/cardinfo.php?archetype=${store.nomeArchetype}`)
          .then((res) => {
            this.store.arrayCards = res.data.data
            // console.log(res.data.data)
          })
      }
    },

    archetypeApi() {
      axios.get('https://db.ygoprodeck.com/api/v7/archetypes.php')
        .then((res) => {
          this.store.arrayType = res.data
          // console.log(res.data)
        })
    }

  }
}
</script>

<template>
  <HeaderComp />
  <TypeSelector @selectEmit="cardsApi" />
  <MainComp />
</template>

<style lang="scss">
@use "./styles/main.scss" as *;
</style>
