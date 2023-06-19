<template>
    <div class="container">
        <div class="row">
            <div class="col-2">
                <AppSingleCard v-for="card in cardList"
                    :cardName="card.name"
                    :cardType="card.type"
                    :cardImage="card.card_images"
                />
            </div>
        </div>
    </div>
</template>
<script>
import AppSingleCard from './AppSingleCard.vue';
import axios from 'axios';
export default {
    name:'AppCardList',
    data(){
        return{
            cardList : [],
        }
    },
    components:{
        AppSingleCard
    },
    created(){
        axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php?num=20&offset=0')
        .then( (response) => {
            // handle success
            console.log(response.data.results);
            this.cardList = response.data.results;
        })
        .catch(function (error) {
            // handle error
            console.log(error);
        });
    }
}
</script>
<style lang="scss" scoped>
    *{
        background-color: white;
    }
</style>