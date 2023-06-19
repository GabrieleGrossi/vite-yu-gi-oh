<template>
  <div>
    <AppHeader/>
    <AppMain/>
  </div>
</template>

<script>
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
export default{
  name: 'App',

  components:{
    AppHeader,
    AppMain
  }
}
</script>

<style lang="scss">
@import "../node_modules/bootstrap/scss/bootstrap";
@import './style/general.scss';
@import './style/partials/mixins' ;
@import './style/partials/variables' ;
</style>
