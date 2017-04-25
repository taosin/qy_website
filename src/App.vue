<template>
  <div id="app">
    <top></top> 
    <router-view></router-view>
  </div>
</template>

<script>
import top from './components/header.vue';
  export default {
    name: 'app',
    components:{
      top
    },
  }
</script>

<style>
  #app {
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    /*color: #2c3e50;*/
    text-align: center;
  }
</style>
