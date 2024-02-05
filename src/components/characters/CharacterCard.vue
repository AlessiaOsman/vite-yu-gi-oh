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
    <div class="character-card rounded p-5">
        <img class="img-fluid rounded-circle mb-4" :src="image" :alt="name">
        <p class="text-center">{{ number }}</p>
        <p class="text-center">{{ name }}</p>
        <p class="text-center">{{ type }}</p>
    </div>
</template>

<style lang="scss" scopeed>
    .character-card{
        background-color: aqua;

        img{
            height: 150px;
        }
    }

</style>


