<template>
    <main>
        <div class="dropdown">
                <button class="btn btn-light dropdown-toggle" type="button" data-bs-toggle="dropdown" aria-expanded="false">
                    Alien
                </button>
                <ul class="dropdown-menu">
                    <li><button class="dropdown-item" type="button">Alien</button></li>
                    <li><button class="dropdown-item" type="button">Another action</button></li>
                    <li><button class="dropdown-item" type="button">Something else here</button></li>
                </ul>
            </div>
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
    .dropdown{
        padding: 30px 15px;
    }
</style>