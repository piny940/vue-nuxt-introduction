<template>
  <ul v-if="existTasks">
    <TodoItem v-for="(title, index) in tasks" :key="index" :title="title" />
  </ul>
  <p v-else>
    No tasks.
  </p>
</template>

<script>
import TodoItem from "./TodoItem";

export default {
  components: {
    TodoItem,
  },
  props: {
    tasks: Array,
  },
  computed: {
    existTasks: function() {
      return this.tasks.length !== 0;
    }
  }
}
</script>
