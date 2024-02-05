<script>
export default{
    name: 'CharacterCard',
    props: {
        image: String,
        number: Number,
        name: String,
        type: String,
        color: String   

    },

    methods: {
        lowerCase(){
            return color.toLowerCase()
        }
    }
}
</script>
<template>
    <div class="character-card rounded p-5" :class="color.toLowerCase()">
        <img class="img-fluid rounded-circle mb-4" :src="image" :alt="name">
        <p class="text-center">{{ number }}</p>
        <p class="text-center"><strong>{{ name }}</strong></p>
        <p class="text-center"><em>{{ type }}</em></p>
    </div>
</template>

<style lang="scss" scopeed>
    .character-card{
        display: flex;
        flex-direction: column;
        align-items: center;

        img{
            height: 150px;
        }
    }

</style>


