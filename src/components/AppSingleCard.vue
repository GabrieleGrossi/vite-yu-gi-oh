<template>
    <div>
        <div class="card" style="width: 18rem;">
            <img :src="image.card_images[0].image_url" class="" :alt='name + "image"'>
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
        image: Image
    }
}
</script>
<style lang="scss" scoped>
    
</style>