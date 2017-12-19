// HTML
<template>
<div class="view">
  <h1>{{title}}</h1>
  <ul>
    <li v-for="item in items" :key=item.index1 :class="{finish:item.isFinished}">{{item.text}}</li>
  </ul>
</div>
</template>

// JS
<script>
export default {
  name: "list",
  // data: function(){
  //   return {

  //   }
  // }
  data() {
    return {
      title: "TodoList",
      items: [
        {
          text: "今天晚上18:00跑步",
          isFinished: false
        },
        {
          text: "今天早餐",
          isFinished: true
        }
      ]
    };
  }
};
</script>

<style>
.view {
  width: 400px;
  border: 1px solid #000;
  margin: 20px auto;
  /* background-color: pink; */
  padding: 20px;
  font-weight: 900;
  /* font-size: 40px; */
}
.finish{
  color: grey;
  text-decoration: line-through;
}
</style>

