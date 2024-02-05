<script>
import {store} from '../../data/store.js'
import CharacterCard from './CharacterCard.vue'
export default {
    name: 'CharactersList',
    data: () => ({
        store
    }),
    components: { CharacterCard } ,
}
</script>
<template>
   <section id="characters" class="my-5">
    <div class="row g-4 row-cols-2 row-cols-md-4 row-cols-lg-5">
        <div class="col" v-for="(character,i) in store.characters" :key="i">
            <CharacterCard 
                :image="character.imageUrl"
                :number="character.number"
                :name="character.name"
                :type="character.type1"
                />
        </div>

    </div>
   </section>
</template>
