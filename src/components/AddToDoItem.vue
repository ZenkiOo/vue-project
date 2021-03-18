<template>
  <form @submit.prevent="OnSubmit">
    <input class="text-input" type="text" v-model="title" />
    <button class="add-button" type="submit">
      Добавить
    </button>
  </form>
</template>

<script>
export default {
  name: 'AddToDoItem',
  data: () => ({
    title: '',
  }),
  methods: {
    OnSubmit() {
      const newToDo = {
        id: Date.now(),
        title: this.title,
        completed: false,
      };
      this.title = '';
      this.$emit('add-todo', newToDo);
    },
  },
};
</script>

<style lang="scss">
.text-input {
  background-color: #444;
  margin-right: 8px;
}
</style>
