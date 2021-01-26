<template>
  <div class="todo-item-wrapper">
     <span class="author">{{ item.author }}</span>
      <span class="todoItem">{{ item.todoItem }}</span>
  </div>
</template>

<script>
export default {
  props: ["item"]

}
</script>

<style>

</style>