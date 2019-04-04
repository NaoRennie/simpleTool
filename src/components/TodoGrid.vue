<template>
  <div class="row">
    <Todo v-for="(todo, index) in todos" :key="index" @click.native="deleteTodo">{{ todo }}</Todo>
  </div>
</template>

<script>
import Todo from "./Todo.vue";
export default {
  Name: "TodoGrid",
  components: {
    Todo
  },
  props: ["todos"],
  methods: {
    deleteTodo(index) {
      this.$emit("todoDelete", index);
    }
  }
};
</script>

<style>
</style>
