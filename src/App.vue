<template>
  <div id="app">

    <headerview> </headerview>
      <img src="./assets/logo.png">


    <ListView />
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld'
import ListView from  './components/list'
import headerview from './components/header'

export default {
  name: 'app',
  components: {
    // HelloWorld
    //註冊組件
    ListView,headerview
  }

}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;

}
</style>
