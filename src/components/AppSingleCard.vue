<template>
    <div>
        <div class="card" style="width: 18rem;">
            <img :src="card_images" class="" alt='name + "image"'>
            <div class="card-body">
                <h4 class="card-title">
                    {{ name }}
                </h4>
                <h4 class="card-text">
                    {{ type }}
                </h4>
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
        card_images: String
    }
}
</script>
<style lang="scss" scoped>
    
</style>