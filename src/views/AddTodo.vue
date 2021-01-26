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
    width: 30rem;
    border: 2px solid black;
    border-radius: 10px;
    margin: 5rem auto auto;
    padding: 2rem;
    display: flex;
  }

  .form {
    margin-left: auto ;
    margin-right: auto;
  }
</style>