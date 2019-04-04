<template>
  <div class="container">
    <form>
      <div class="ui list">
        <div class="item">
          <label>To Do List</label>
        </div>
        <div class="item">
          <textarea rows="3" v-model="todo"></textarea>
        </div>
        <div class="item">
          <button class="ui button" @click.prevent="createNew">add</button>
        </div>
      </div>
    </form>
  </div>
</template>

<script>
import Todo from "./Todo.vue";
export default {
  Name: "NewTodo",
  data() {
    return {
      todo: ""
    };
  },
  methods: {
    createNew() {
      this.$emit("todoAdded", this.todo);
      this.todo = "";
    }
  }
};
</script>

<style>
.container {
  text-align: center;
}
textarea {
  width: 500px;
  height: 50px;
}
</style>
