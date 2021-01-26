<template>
  <div class="AddTodo">
    <div class="form">
      <AddToTodoList />
    </div>
    
  </div>
</template>

<script>
import AddToTodoList from "../components/AddToTodoList"

export default {
  components: {
    AddToTodoList,
  }
  
}
</script>

<style scooped>
  .AddTodo {
    border: 2px solid black;
    border-radius: 10px;
    margin: 1rem 1rem;
    padding: 2rem;
    display: flex;
  }

  .form {
    margin-left: auto ;
    margin-right: auto;
  }
</style>