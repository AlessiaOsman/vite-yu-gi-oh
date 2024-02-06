<script>
import FilterSelect from './selectForm/FilterSelect.vue';
export default {
    name: 'AppHeader',
    components: {FilterSelect}

}
</script>
<template>
    <header class="container d-flex justify-content-between align-items-center">
    <h1 class="text-center mt-4 cols-10">Pokévuex</h1>
    <FilterSelect/>
  </header>
</template>
<style>
</style>