<template>
  <div id="app">
    <mainHeader />
  </div>
</template>

<script>
import mainHeader from './components/MainHeader.vue';

export default {

  name: 'App',
  components: {
    mainHeader,

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
