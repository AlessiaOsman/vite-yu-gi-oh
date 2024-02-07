<script>
import axios from 'axios'
import { store } from './data/store.js'
const endpoint = 'https://41tyokboji.execute-api.eu-central-1.amazonaws.com/dev/api/v1/pokemons'
import AppMain from './components/AppMain.vue'
import AppHeader from './components/AppHeader.vue'
export default {
  name: 'Pokemon',
  components: { AppMain, AppHeader },
  methods:{
    fetchTypes(){
      axios.get(endpoint + '/types1').then(res => {
        store.types = res.data.map((type, i) => {
          return {
            label: type,
            value: type,
            id: i
          }
        })
      })
    },

    fetchPokemon(){
      axios.get(endpoint).then(res => {
      store.pokemons = res.data.docs;
    })
    },

    filterPokemon(type){
      const endpoint = type ? `${endpoint}?eq[type1]=${type}` : endpoint;
      this.fetchPokemon()

    }
  },
  
  created(){
    this.fetchPokemon();
    this.fetchTypes();
  } 
}
</script>

<template>
  <AppHeader @type-change="filterPokemon"/>
  <AppMain />
</template>

<style lang="scss">
@use'./assets/scss/style.scss';
</style>
