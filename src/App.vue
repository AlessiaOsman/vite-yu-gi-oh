<script>
import axios from 'axios'
import { store } from './data/store.js'
const endpoint = 'https://41tyokboji.execute-api.eu-central-1.amazonaws.com/dev/api/v1/pokemons'
import AppMain from './components/AppMain.vue'
export default {
  name: 'Pokemon',
  components: { AppMain },
  created(){
    axios.get(endpoint).then(res => {
      store.pokemons = res.data.docs;
    })
  }
}
</script>

<template>
  <header>
    <h1 class="text-center mt-4">Pokévuex</h1>
  </header>
  <AppMain />
</template>

<style lang="scss">
@use'./assets/scss/style.scss';
</style>
