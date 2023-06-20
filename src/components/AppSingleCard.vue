<template>
    <div class="my-cards-element">
        <img :src="singleCard.card_images[0].image_url" :alt="singleCard.name + 'Image'">
        <h3>{{ singleCard.name }}</h3>
        <span>{{ singleCard.archetype }}</span>
    </div>
</template>
<script>
export default {
    name:'AppSingleCard',
    data(){
        return{

        }
    },
    props:{
        singleCard: Object,
    }
}
</script>
<style lang="scss" scoped>
    
.my-cards-element {
    background-color: #d48f38;
    width: calc(100% / 5 - 1.2rem);
    height: 500px;
    margin: 1.2rem 0;
    text-align: center;
    border-radius: 0 0 20px 20px;

    img {
        width: 100%;
    };

    h3 {
        color: white;
        text-transform: uppercase;
        margin: .5rem;
    }

    span {
        display: inline-block;
        margin: .5rem;
    }
}
</style>