<template>
  <div>
    <div v-bind:key="oneTodo.id" v-for="oneTodo in todoList">
      <TodoItem v-bind:todo="oneTodo" v-on:del-todo="$emit('del-todo',oneTodo.id)"/>
    </div>
  </div>
</template>

<script>
import TodoItem from "./TodoItem";

export default {
  name: "Todos",
  components: {
    TodoItem
  },
  props: ["todoList"]
};
</script>

<style scoped>
</style>
