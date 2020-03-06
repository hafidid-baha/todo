<template>
  <div id="app">
    <div class="container">
      <AddTodo />
      <Todos />
    </div>
  </div>
</template>

<script>
//import HelloWorld from './components/HelloWorld.vue'
import Todos from './components/Todos.vue'
import AddTodo from './components/AddTodo.vue'

export default {
  name: 'App',
  components: {
    Todos,AddTodo
  }
}
</script>

<style>
body{
  font-family: 'Poppins', sans-serif;
  background: #e9f3f2;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.todo{
  background: lightseagreen;
  color: white;
  text-transform: capitalize;
  font-family: 'Poppins', sans-serif;
  min-height: 100px;
}
</style>
