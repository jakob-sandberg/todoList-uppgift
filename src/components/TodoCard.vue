<template>
  <div class="todo-card" @click="deleteTodo">
    <div class="author-wrapper">
      <span class="author">Author:  {{ todoitem.author }}</span>
   </div>   
   <div class="todo-wrapper">
   <span class="todo">What needs to be done:  {{ todoitem.todoItem }}</span>
   </div>
    
  </div>
</template>

<script>
export default {
  props: ["todoitem"],

  methods: {
    deleteTodo() {
      console.log("To Remove: ", this.todoitem);
      this.$emit("removeTodo", this.todoitem);
    },
  },
};
</script>

<style scoped>
.todo-card {
  border: 2px solid black;
  border-radius: 10px;
  cursor: pointer;
  display: flex;
  flex-direction: column;
  margin: 1rem 1rem;
  padding: 0.5rem;
}

.wrapper {
  display: flex;
}

.title-rating {
  justify-content: space-between;
}

.genre {
  justify-content: flex-end;
}
</style>
