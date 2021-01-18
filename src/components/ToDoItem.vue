<template>
  <li>
    <span>
      <label :for="'checkbox' + todo.id">
        <input :id="'checkbox' + todo.id" type="checkbox" />
        <strong>{{ todo.id }}</strong>
        {{ todo.title }}
      </label>
      <button>&times;</button>
    </span>
  </li>
</template>

<script>
export default {
  props: {
    todo: {
      type: Object,
      requered: true
    }
  }
};
</script>
