<template>
    <div class="container">
        <div class="row flex">
            <div class="col-2">
                <AppSingleCard v-for="card in cardList"
                    :name="card.name"
                    :type="card.type"
                    :image="card.card_images"
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
            console.log(response.data.data);
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
    *{
        background-color: white;
    }
</style>