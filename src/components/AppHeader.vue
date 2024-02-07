<script>
import FilterSelect from './select/FilterSelect.vue';
import {store} from '../data/store.js'
export default {
    name: 'AppHeader',
    components: {FilterSelect},
    data: () => ({
      store
    }),
    emits: ['type-change']

}
</script>
<template>
    <header class="container d-flex justify-content-between align-items-center">
    <h1 class="text-center mt-4 cols-10">Pokévuex</h1>
    <FilterSelect default-label="Tutti" :options="store.types" @option-change="$emit('type-change', $event)" />
  </header>
</template>
<style>
</style>