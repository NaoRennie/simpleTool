<template>
  <div class="header-container">
    <div class="bar" :style="{width: width() }">{{ todoCount }} / {{ maxTodos }}</div>
  </div>
</template>

<script>
export default {
  name: "Header",
  props: ["todoCount", "maxTodos"],
  methods: {
    width() {
      this.todoCount > 0 ? todoCount * 70 + "px" : 50 + "px";
    }
  }
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
