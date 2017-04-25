<template>
  <div id="app">
    <top></top> 
    <router-view></router-view>
    <foot></foot>
  </div>
</template>

<script>
import top from './components/header.vue';
import foot from './components/footer.vue';
  export default {
    name: 'app',
    components:{
      top,
      foot
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
    background: #dedede;
    width: 100%;
    height: 100%;
  }
</style>
