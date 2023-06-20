<template>
    <main>
        <AppSearchbar/>
        <AppCardList/>
    </main>
</template>
<script>
import AppSearchbar from './AppSearchbar.vue'
import AppCardList from './AppCardList.vue';
export default {
    name: 'AppMain',
    components:{
    AppCardList,
    AppSearchbar
    },
        
}
</script>
<style lang="scss" scoped>
    main{
        background-color: #d48f38;
    }
</style>