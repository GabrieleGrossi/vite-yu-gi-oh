<template>
    <div class="my-searchbar">
        <select name="card-archetype" @change="$emit('eventChangeType', $event.target.value)">
            <option selected hidden> Select an archetype</option>
            <option v-for="archetype in archetypeList" :value="archetype.archetype_name">

                {{ archetype.archetype_name }}
            </option>
        </select>
    </div>
</template>
<script>
export default {
    name: 'AppSearchbar',
    props:{
        archetypeList: Array
    },
    data(){
        return{

        }
    },
}
</script>
<style lang="scss" scoped>
    
    .my-searchbar {
        width: 80%;
        margin: 0 auto;
        padding: 1.5rem 0;
    }
    select{
        border-radius: 15px;
        text-align: center;
        padding: 0.5rem;
        border: 1px solid transparent;
    }
</style>