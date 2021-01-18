<template>
  <div>
    <ul>
      <ToDoItem 
      v-for="todo of todos" 
      :todo="todo" 
      :key="todo.id" 
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
  }
};
</script>
