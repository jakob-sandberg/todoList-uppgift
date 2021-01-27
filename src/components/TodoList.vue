<template>
  <div class="todo-list">
    <div v-if="todos.length > 0">
      <TodoCard
        v-for="(todoitem, i) in todos"
        :key="i"
        :todoitem="todoitem"
        @removeTodo="removeTodo"
      />
    </div>
  </div>
</template>

<script>
import TodoCard from "./TodoCard";

export default {

  components: {
    TodoCard,
  },
  

  props: ["newTodo"],

  watch: {
    newTodo: function(newTodo, oldVal) {
      console.log("Old value: ", oldVal);
      console.log("New value: ", newTodo);
      this.todos.unshift(newTodo);
    },
  },

  data() {
    return {
      todos: [
        {
          author: "James Bond",
          todoItem: "Be Awesome",
        },
        {
          author: "Q",
          todoItem: "Invent shit",
        },
        {
          author: "Moneypenny",
          todoItem: "Get into Bonds Pants",
        },
      ],
    };
  },

  methods: {
    addTodoToTodos(newTodo) {
      this.movies.push(newTodo);
      console.log("In App.vue - movies: ", this.todos);
    },
    removeTodo(todoToRemove) {
      console.log("In movielist", todoToRemove);
      this.todos = this.todos.filter((todo) => todoToRemove !== todo);
    },
  },
};
</script>

<style scooped>
  .todo-list {
  border: 2px solid black;
  border-radius: 10px;
  display: flex;
  flex-direction: column;
  margin: auto auto;
  padding: 0.5rem;
  }
</style>