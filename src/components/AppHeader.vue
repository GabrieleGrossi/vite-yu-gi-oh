<template>
    <header>
        <img src="../assets/img/MtG_logo.jpg" alt="Correct logo">  
        <h1>
            Yu-Gi-Oh Api is for children
        </h1>  
    </header>
</template>
<script>
export default {
    name: 'AppHeader'
}
</script>
<style lang="scss" scoped>
    @use '../style/general' as *;
    @use '../style/partials/variables' as *;
    @use '../style/partials/mixins' as *;

    header {
        @include flex(row, start, center, no-wrap);
        padding: 1rem;

        img {
            width: 250px;
        };

        h1 {
            margin-left: 1.5rem;
        }
    }
</style>