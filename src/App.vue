<template>
  <h1>Todo List</h1>
  <ul>
    <li v-for="item in ToDoItems" :key="item.id">
      <to-do-item :label="item.label" :done="item.done"></to-do-item>
    </li>
  </ul>
</template>

<script>
import ToDoItem from "./components/ToDoItem.vue";
import uniqueId from "lodash.uniqueid";

export default {
  name: "App",
  components: { ToDoItem },
  data() {
    return {
      ToDoItems: [
        { id: uniqueId("todo-"), label: "Study JS", done: true },
        { id: uniqueId("todo-"), label: "Study TS", done: false },
        { id: uniqueId("todo-"), label: "Prepare for exams", done: true },
        { id: uniqueId("todo-"), label: "Write the thesis", done: false },
        { id: uniqueId("todo-"), label: "Learn C++", done: false },
      ],
    };
  },
};
</script>

<style scoped></style>
