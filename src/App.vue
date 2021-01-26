<template>
  <div id="app">
    <Navbar />
    <TodoItem />
    <router-view/>
  </div>
</template>

<script>
import Navbar from "./components/Navbar"
import TodoItem from "./components/TodoItem"

export default {
  components: {
    Navbar,
    TodoItem,
  },

  data() {
    return {
      newTodoItem: null
      }
  },

  methods: {
    sendNewTodoToStart(item) {
      this.newTodoItem = item;
    }
  }
  
}
</script>



<style scooped>
  * {
    box-sizing: border-box;
  }

  body {
    background: darkolivegreen;
  }
</style>
