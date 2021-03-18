<template>
  <div>
    <h2>Todo App</h2>
    <hr />
    <AddToDoItem @add-todo="AddToDo" />
    <ToDoList v-bind:todos="todos" @remove-todo="RemoveTodo" />
  </div>
</template>

<script>
import ToDoList from '@/components/ToDoList.vue';
import AddToDoItem from '@/components/AddToDoItem.vue';

export default {
  name: 'Todos',
  data: () => ({
    todos: [],
  }),
  components: {
    ToDoList,
    AddToDoItem,
  },
  methods: {
    RemoveTodo(id) {
      this.todos = this.todos.filter((t) => t.id !== id);
    },
    AddToDo(obj) {
      this.todos.push(obj);
    },
  },
  mounted() {
    fetch('https://jsonplaceholder.typicode.com/todos')
      .then((response) => response.json())
      .then((json) => (this.todos = json));
  },
};
</script>

<style></style>
