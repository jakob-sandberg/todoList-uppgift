<template>
  <div class="todolistform">
    <form @submit.prevent="createTodo">
    <div class="author-wrapper">
        <label for="author">Author</label>
        <input class="author-input" type="text" 
        id="author" 
        name="author" 
        placeholder="Author" 
        v-model="author">
    </div>
    <div class="add-todo-item-wrapper">
    <label for="todo-item">Add todo</label>
    <input class="todo-input" type="text" 
    name="todoItem" 
    placeholder="What needs to be done?" 
    v-model="todoItem">
    </div>
    <div>
      <button>Add</button>
    </div>

    </form>
  </div>
</template>

<script>
export default {
  data() {
    return {
      author: "",
      todoItem: "",
    }
  },
  
  methods: {
    createTodo() {
      let newTodoItem = {
        author: this.author,
        todoItem: this.todoItem
      }
      console.log(newTodoItem);
      
      this.$emit("add-todo", newTodoItem)
    }
  }

}
</script>

<style scooped>

  .add-todo-item-wrapper {
    margin-top: 1rem;
  }

  .todo-input {
    margin-left: 20px;
  }

  .author-input {
    margin-left: 35px;
  }

button {
   margin-top: 20px;
   margin-left: auto;
   margin-right: auto;
  }
</style>