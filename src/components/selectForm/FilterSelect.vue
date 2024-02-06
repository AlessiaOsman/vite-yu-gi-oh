<script>
export default{
    name: 'FilterSelect',
    data: ()=>({
        types: [
            "Bug",
            "Dark",
            "Dragon",
            "Electric",
            "Fairy",
            "Fighting",
            "Fire",
            "Flying",
            "Ghost",
            "Grass",
            "Ground",
            "Ice",
            "Normal",
            "Poison",
            "Psychic",
            "Rock",
            "Steel",
            "Water"
        ]
    })
}
</script>

<template>
    <select class="form-select mt-4 select-form">
        <option selected>All</option>
        <option v-for="type in types">{{ type }}</option>
    </select>
</template>



