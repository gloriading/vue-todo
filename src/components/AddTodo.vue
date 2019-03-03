<template>
  <div id="addTodo">
    <form @submit="addTodo">
      <input type="text" v-model="title" name="title" placeholder="Add Todo">
      <input type="submit" value="Submit" class="submit-btn">
    </form>
  </div>
</template>

<script>
// import uuid from "uuid";

export default {
  name: "AddTodo",
  data() {
    return {
      title: ""
    };
  },
  methods: {
    addTodo(e) {
      e.preventDefault();
      const userInput = this.title.trim();
      if (userInput === "") {
        alert("Please enter one todo-task before pressing submit button");
      } else {
        const newTodo = {
          // id: uuid.v4(),
          title: userInput,
          completed: false
        };
        this.$emit("add-todo", newTodo);
        this.title = "";
      }
    }
  }
};
</script>

<style scoped>
#addTodo {
  margin-bottom: 10px;
}

form {
  display: flex;
}

input[type="text"] {
  flex: 10;
  padding: 10px 10px 10px 50px;
  border-top: 1px solid #4d5656;
  border-bottom: 1px solid #4d5656;
  background-color: #f2f3f4;
  outline: none;
  font-size: 14px;
}

input[type="text"]:focus {
  background-color: #fdfefe;
  border-top: 1px solid MEDIUMSEAGREEN;
  border-bottom: 1px solid MEDIUMSEAGREEN;
}

input[type="submit"] {
  flex: 2;
  cursor: pointer;
  background-color: #4d5656;
  font-size: 18px;
  color: whitesmoke;
  transition: 0.2s;
  outline: none;
}

input[type="submit"]:hover {
  color: MEDIUMSEAGREEN;
}
</style>
