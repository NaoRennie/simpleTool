<template>
  <div class="header-container">
    <div class="bar" :style="{width: todoCount*60 +'px' }">{{ todoCount }} / {{ maxTodos }}</div>
  </div>
</template>

<script>
export default {
  name: "Header",
  props: ["todoCount", "maxTodos"]
};
</script>

<style>
.bar {
  display: inline-block;
  width: 50px;
  height: 50px;
  background-color: #eee;
}
.header-container {
  text-align: left;
}
</style>
