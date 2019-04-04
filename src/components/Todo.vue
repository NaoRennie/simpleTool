<template>
  <div>
    <div class="panel-container">
      <div class="panel-body todo">
        <slot></slot>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Todo"
};
</script>

<style scoped>
.panel-body {
  font-size: 24px;
  color: #6e6e6e;
  display: inline-block;
  height: 150px;
  width: 250px;
  border: thick double #32a1ce;
}
.todo {
  cursor: pointer;
}
.todo:hover {
  background-color: #ffe2e2;
}
.panel-container {
  float: left;
}
</style>
