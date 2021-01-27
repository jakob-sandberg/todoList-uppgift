<template>
  <div class="home">
    <h1>Todo List</h1>
    <TodoList />
  </div>
</template>

<script>
import TodoList from "../components/TodoList"

export default {
  components: {
    TodoList,
  },
  
  
  
}
</script>

<style scoped>
  .home {
    display: grid;
  }

  h1 {
    margin-left: auto;
    margin-right: auto;
  }
</style>
