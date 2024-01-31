<template>
  <form @submit="onSubmit">
    <label for="new-todo-input">What should be done?</label>
    <input
      type="text"
      id="new-todo-input"
      name="new-todo"
      autocomplete="off"
      v-model.lazy.trim="label"
    />
    <button type="submit">Add new task</button>
  </form>
</template>

<script>
export default {
  methods: {
    onSubmit() {
      this.$emit("todo-added");
    },
  },
  data() {
    return { label: "" };
  },
};
</script>

<style scoped></style>
