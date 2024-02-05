<script>
  import AppMain from './components/AppMain.vue'
  export default {
    name: 'App',
    components: {AppMain}
  }
</script>

<template>
  <header>
    <h1 class="text-center mt-4">Pokévuex</h1>
  </header>
  <AppMain/>
</template>

<style lang="scss">
  @use'./assets/scss/style.scss'
</style>
