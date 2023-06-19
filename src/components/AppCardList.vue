<template>
    <div>
        <h2>
            App Card List
        </h2>
        <AppSingleCard/>
    </div>
</template>
<script>
import AppSingleCard from './AppSingleCard.vue';
export default {
    name:'AppCardList',
    components:{
        AppSingleCard
    },
    created(){

    }
}
</script>
<style lang="scss" scoped>
    *{
        background-color: white;
    }
</style>