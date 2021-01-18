<template>
  <div id="app">
    <h1>Todo App</h1>
    <hr>
    <ToDoList 
    v-bind:todos='todos'
    />
  </div>
</template>

<script>
import ToDoList from '@/components/ToDoList.vue'

export default {
  name: 'App',
  data() {
    return {
      todos: [
        {id: 1, title: 'Купить хлеб', completed: false},
        {id: 2, title: 'Купить молоко', completed: false},
        {id: 3, title: 'Купить соль', completed: false}
      ]
    }
  },
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
