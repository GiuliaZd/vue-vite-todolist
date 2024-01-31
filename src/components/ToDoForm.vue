<template>
  <form @submit="onSubmit">
    <label for="new-todo-input">What should be done?</label>
    <input
      type="text"
      id="new-todo-input"
      name="new-todo"
      autocomplete="off"
      v-model="label"
    />
    <button type="submit">Add new task</button>
  </form>
</template>

<script>
export default {
  methods: {
    onSubmit() {
      console.log("labelin arvo:", this.label);
    },
  },
  data() {
    return { label: "" };
  },
};
</script>

<style scoped></style>
