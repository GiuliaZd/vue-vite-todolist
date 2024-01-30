<template>
  <h1>Todo List</h1>
  <ul>
    <li>
      <to-do-item label="Todo task" :done="true"></to-do-item>
    </li>
  </ul>
</template>

<script>
import ToDoItem from "./components/ToDoItem.vue";

export default {
  name: "App",
  components: { ToDoItem },
};
</script>

<style scoped></style>
