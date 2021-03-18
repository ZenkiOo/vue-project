<template>
  <li>
    <span>
      <label :for="'checkbox' + todo.id">
        <input
        :id="'checkbox' + todo.id"
        type="checkbox"
        class="todoinput"
        @change="todo.completed = !todo.completed"
         />
        <span class="todo-text" v-bind:class="{completed: todo.completed}">
          <strong>{{ todo.id }} || </strong>
          {{ todo.title }}
        </span>
      </label>
      <button
      @click="$emit('remove-todo', todo.id)"
      >&times;</button>
    </span>
  </li>
</template>

<script>
export default {
  // Альтернативный список PROPS
  // props: {
  //   todo: {
  //     type: Object,
  //     requered: true,
  //   },
  // },
  props: ['todo'],
};
</script>
<style lang="scss">
.todoinput {
  display: none;
  &:checked {
    ~ .todo-text {
      color: #222;
    }
  }
}
.completed {
  text-decoration: line-through;
}
</style>
