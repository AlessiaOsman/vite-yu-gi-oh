<script>
export default{
    name: 'CharacterCard',
    props: {
        image: String,
        number: Number,
        name: String,
        type: String    

    }
}
</script>
<template>
    <div id="character-card">
        <img :src="image" :alt="name">
        <p>{{ number }}</p>
        <p>{{ name }}</p>
        <p>{{ type }}</p>
    </div>
</template>
