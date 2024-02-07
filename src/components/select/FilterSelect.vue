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
        ],

        typeSelected: ''
    })
}
</script>

<template>
    <select v-model="typeSelected">
        <option disabled value="">Please select one</option>
        <option v-for="type in types">{{ type }}</option>
    </select>
    <p>{{ typeSelected }}</p>
</template>
