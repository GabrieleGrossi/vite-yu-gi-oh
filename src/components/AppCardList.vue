<template>
    <div class="container">
        <div class="row">
            <div class="col-2">
                <AppSingleCard v-for="card in cardList"
                    :name="card.name"
                    :type="card.type"
                    :image="card.card_images[0].image_url"
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
            apiUrl:'https://db.ygoprodeck.com/api/v7/cardinfo.php?num=20&offset=0', 
            cardList : [],
        }
    },
    components:{
        AppSingleCard
    },
    created(){
        axios.get(this.apiUrl)
        .then( (response) => {
            // handle success
            console.log(response.data.data[0].card_images);
            this.cardList = response.data.data;
        })
        .catch(function (error) {
            // handle error
            console.log(error);
        });
    }
}
</script>
<style lang="scss" scoped>
@use '../style/partials/mixins';
    *{
        background-color: white;
    }
    .row{
        display: flex;
        flex-direction: row;
    }
</style>