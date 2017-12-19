// HTML
<template>
<div class="view">
  {{
    title
  }}
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
      title: "TodoList"
    };
  }
};
</script>

<style>
.view {
  width: 400px;
  border: 1px solid #000;
  margin: 20px auto;
  background-color: pink;
  padding: 20px;
}
</style>

