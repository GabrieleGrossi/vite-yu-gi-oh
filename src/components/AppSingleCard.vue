<template>
    <div class="my-cards-element">
        <img :src="singleCard.card_images[0].image_url" :alt="singleCard.name + 'Image'">
        <h4>
            {{ singleCard.name }}
        </h4>
        <span>
            {{ singleCard.archetype }}
        </span>
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
    img {
        width: 100%;
    };
    h4 {
        color: white;
        text-transform: uppercase;
        margin: .5rem;
    };
    span {
        display: inline-block;
        color: white
    };
    &:hover{
            background-color: black;
            transition: 0.7s ease-in;
        };
}
</style>