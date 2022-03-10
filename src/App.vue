<template>
  <div id="app">
    <mainHeader />
    <mainContent />
  </div>
</template>

<script>
import mainHeader from './components/MainHeader.vue';
import mainContent from './components/MainContent.vue';


export default {

  name: 'App',
  components: {
    mainHeader,
    mainContent,
  }
}
</script>

<style lang="scss">
@import './assets/scss/common.scss';

#app {
  font-family: "Montserrat";
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
</style>
