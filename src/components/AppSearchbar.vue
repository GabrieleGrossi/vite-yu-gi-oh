<template>
    <div>
        <select class="form-select" aria-label="Default select example">
            <option selected>
                Select a card type
            </option>
            <option value="1">
                One
            </option>
            <option value="2">
                Two
            </option>
            <option value="3">
                Three
            </option>
        </select>
    </div>
</template>
<script>
export default {
    name: 'AppSearchbar'
}
</script>
<style lang="scss" scoped>
    select{
        width: 20%;
        margin: 0 auto;
        margin-top: 1rem;
    }
</style>