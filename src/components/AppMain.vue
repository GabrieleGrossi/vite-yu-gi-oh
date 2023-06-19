<template>
    <main>
        <h1>App Main</h1>
        <AppCardList/>
    </main>
</template>
<script>
import AppCardList from './AppCardList.vue';
export default {
    name: 'AppMain',
    components:{
    AppCardList,
    },
        
}
</script>
<style lang="scss" scoped>
    main{
        background-color: #d48f38;
    }
</style>