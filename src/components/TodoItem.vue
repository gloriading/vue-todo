<template>
  <div class="todo-item">
    <h4 v-bind:class="{'is-complete':todo.completed}">
      <input type="checkbox" v-on:change="markComplete">
      {{todo.title}}
    </h4>
    <button class="del" @click="$emit('del-todo', todo.id)">x</button>
  </div>
</template>

<script>
export default {
  name: "TodoItem",
  props: ["todo"],
  methods: {
    markComplete() {
      this.todo.completed = !this.todo.completed;
    }
  }
};
</script>

<style scoped>
.todo-item {
  padding: 10px;
  background-color: #d7dbdd;
  color: #333;
  margin-bottom: 1px;
  transition: 0.5s ease;
  cursor: crosshair;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
}

.todo-item:hover {
  background-color: #f2f3f4;
}

h4 {
  font-size: 16px;
  letter-spacing: 2px;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
}

input[type="checkbox"] {
  margin-right: 5px;
}

.is-complete {
  text-decoration: line-through MEDIUMSEAGREEN wavy;
}

.del {
  outline: none;
  font-size: 20px;
  width: 30px;
  height: 30px;
  border: 1px solid #333;
  border-radius: 50%;
  background-color: transparent;
  color: #333;
  margin-left: 2rem;
}

.del:hover {
  background-color: white;
  color: #333;
}
</style>
