<template>
    <div class="my-cards-list">
        <h2>I have found {{ store.listApi.length }} cards</h2>
        <AppSingleCard v-for="card in store.listApi"
            :singleCard="card"
        />
    </div>
</template>
<script>
import AppSingleCard from './AppSingleCard.vue';
import { store } from '../store.js';
export default {
    name: "AppCardList",
    components: { 
        AppSingleCard
    },
    data () {
        return {
            store
        }
    },
}
</script>
<style lang="scss" scoped>
@import '../style/partials/mixins';
.my-cards-list {
        @include flex(row, space-between, start, wrap);
        background-color: white;
        padding: 3rem;
        width: 80%;
        margin: 0 auto;
        overflow: scroll;
        max-height: 100vh;

        h2 {
            background-color: black;
            color: white;
            padding: 1rem;
            flex-basis: 100%;
            border-radius: 10px;
        }
    }
</style>