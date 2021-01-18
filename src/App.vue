<template>
  <div id="app">
    <h1>Todo App</h1>
    <ToDoList />
  </div>
</template>

<script>
import ToDoList from '@/components/ToDoList.vue'

export default {
  name: 'App',
  components: {
    ToDoList
  },
};
</script>

<style lang="scss">
body {
  background-color: #333;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #999;
  margin-top: 60px;
}
</style>
