<template>
    <div class="my-searchbar">
        <select name="card-archetype">
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
    }
}
</script>
<style lang="scss" scoped>
    
    .my-searchbar {
        width: 50%;
        margin: 0 auto;
        padding: 1.5rem;
    }
</style>