<template>
  <div>
    <ul>
      <ToDoItem 
      v-for="todo of todos" 
      :todo="todo" 
      :key="todo.id"
      @remove-todo="RemoveTodo"
      />
    </ul>
  </div>
</template>

<script>
import ToDoItem from "@/components/ToDoItem.vue";
export default {
  props: ["todos"],
  components: {
    ToDoItem
  },
  methods: {
    RemoveTodo(id) {
      this.$emit('remove-todo', id)
    },
  },
};
</script>
