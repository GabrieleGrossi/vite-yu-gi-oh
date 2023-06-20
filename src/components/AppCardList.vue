<template>
    <section>
        <div class="my-container black">
            <div class="my-row">
                <div class="col-12 my-search">
                    <h2>
                        You found {{ cardList.length }} cards
                    </h2>
                </div>
            </div>
        </div>
        <div class="my-container">
            <div class="row">
                <div class="col-12 d-flex flex-wrap ">
                    <AppSingleCard v-for="card in cardList"
                        :name="card.name"
                        :type="card.type"
                        :image="card.card_images[0].image_url"
                    />
                </div>
            </div>
        </div>
    </section>
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
    section{
        background-color: white;
        width: 80%;
        margin: 0 auto;
    }
    .my-container{
        width: 80%;
        margin: 0 auto;
        
    }
    .my-row{
        width: 50%;
        margin-top: 2rem;
    }
    .my-search{
        padding-top: 2rem;
    }
    .black{
        background-color: black;
        color: white;
        width: calc(100% - 6rem);
    }
</style>