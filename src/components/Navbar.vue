<template>
  <div class="navbar">
    <router-link to="/">Home</router-link>
    <router-link to="/about">About</router-link>
    <router-link to="/AddTodoPage">Add Todo</router-link>
  </div>
</template>

<script>
export default {

}
</script>

<style scooped>
  .navbar {
  background: lightgrey;
  padding: 0.6rem 0 0.6rem
 }

a {
  color: black;
  font-size: 1.5rem;
  text-decoration: none;
  margin: 0 1rem;
  transition: 0.3s;
}

a:hover {
  color: grey;
}
</style>