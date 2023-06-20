<template>
    <main>
        <AppSearchbar
        :archetypeList="archetypeList"
        @eventChangeType="archetypeChange"/>
        <AppCardList/>
    </main>
</template>
<script>
import AppSearchbar from './AppSearchbar.vue'
import AppCardList from './AppCardList.vue';
import axios from 'axios';
import { store } from '../store.js';
export default {
    name: 'AppMain',
    components:{
    AppCardList,
    AppSearchbar
    },

    data(){
        return{
            archetypeList:[],
        }
    },
    methods: {
        archetypeChange(archetype) {
            axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php?archetype=' + archetype)
            .then(function (response) {
                    console.log(response.data.data);
                        store.listApi = response.data.data;
                    })
                    .catch(function (error) {
                        console.log(error);
                    })
        }
    },
    created(){
        axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php?num=20&offset=0')
            .then(function (response) {
                console.log(response.data.data);
                store.listApi = response.data.data;
            })
            .catch(function (error) {
                console.log(error);
            }),

        axios.get('https://db.ygoprodeck.com/api/v7/archetypes.php')
            .then(response => {
                console.log(response.data);
                this.archetypeList = [...response.data];
            })
            .catch(function (error) {
                console.log(error);
            })
    }
        
}
</script>
<style lang="scss" scoped>

    main {
        background-color: #d48f38;
        padding: 1rem;
    }
</style>