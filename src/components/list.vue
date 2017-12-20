// HTML
<template>
<div class="view">
  <h1 class="title">{{title}}</h1>
  <input type="text" @keyup.enter="addData" v-model="newStr">
  <ul>
    <li v-for="item in items" :key=item.index1 :class="{finish:item.isFinished}" @click="toggleFinish(item)">{{item.text}}</li>
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
      ],
      newStr: ""
    };
  },
  methods: {
    toggleFinish: function(item) {
      item.isFinished = !item.isFinished;
    },
    addData: function() {
      console.clear();
      console.log(this.newStr);
      this.items.push( {
          text: this.newStr,
          isFinished: false
        })
        this.newStr='';
    }
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
.view .title {
  border-bottom: 1px solid #000;
}
.view ul li {
  margin: 10px 0;
  list-style: none;
}
.view .finish {
  color: grey;
  text-decoration: line-through;
}
</style>

