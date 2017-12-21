<template>
  <div id="app">

    <headerview :msg="title"> </headerview>
      <img src="./assets/logo.png">


    <ListView  @myMsg="getData"/>
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld'
import ListView from  './components/list'
import headerview from './components/header'

//app.vue是父組件，listview是子組件  組件間通信
// 父組件 --> 子組件   props選項
//子組件  --> 父組件   自定義事件


export default {
  name: 'app',
  components: {
    // HelloWorld
    //註冊組件
    ListView,headerview
  },
  data(){
    return {
      title : "Vue入門學習"
    }
  },
  methods: {
    getData(msg){
      // console.log("App.vue組件");
     this.title = msg;
    }
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
