<template>
    <div class="container-image">
        <div class="card">
            <img :src="image" class="card-img-top" :alt='name + "image"'>
            <div class="card-body">
                <h4 class="card-title">
                        {{ name }}
                </h4>
                <h5 class="card-text">
                        {{ type }}
                </h5>
            </div>
        </div>
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
        name: String,
        type: String,
        image: String
    }
}
</script>
<style lang="scss" scoped>
    .card {
    height: 100%;
    width: 150px;
    margin-left: 2.7rem;
    background-color: #d48f38;
    }
    .container-image{
        margin-bottom: 2rem;
    }
</style>