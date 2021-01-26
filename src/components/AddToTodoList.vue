<template>
  <div class="todolistform">
    <form @submit.prevent="createTodo">
    <div class="author-wrapper">
        <label for="author">Author</label>
        <input type="text" 
        id="author" 
        name="author" 
        placeholder="Author" 
        v-model="author">
    </div>
    <div class="add-todo-item-wrapper">
    <label for="todo-item">Add todo</label>
    <input type="text" 
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
    }
  }

}
</script>

<style scooped>


</style>