<template>
  <div class="container">
    <NewTodo @todoAdded="newTodo"></NewTodo>
    <Header :todoCount="todos.length" :maxTodos="maxTodos"></Header>
    <TodoGrid :todos="todos" @todoDelete="todoDeleted(index)"></TodoGrid>
  </div>
</template>

<script>
import TodoGrid from "./components/TodoGrid.vue";
import NewTodo from "./components/NewTodo.vue";
import Header from "./components/Header.vue";

export default {
  name: "App",
  components: {
    TodoGrid,
    NewTodo,
    Header
  },
  data() {
    return {
      todos: [],
      maxTodos: 10
    };
  },
  methods: {
    newTodo(todo) {
      this.todos.length >= this.maxTodos
        ? alert("please delete one")
        : this.todos.push(todo);
    },
    todoDeleted(index) {
      this.todos.splice(index, 1);
    }
  }
};
</script>

<style>
</style>
