<template>
  <div id="app">
    <h1>Todoアプリ</h1>
    <TodoInput id="todo-input" :addTodo="addTodo" />
    <ResetTasks id="reset-tasks" :resetTasks="resetTasks" />
    <TodoList id="todo-list" :tasks="tasks"/>
  </div>
</template>

<script>
import TodoList from "./components/TodoList.vue";
import TodoInput from "./components/TodoInput.vue";
import ResetTasks from "./components/ResetTasks.vue";

export default {
  components: {
    TodoList,
    TodoInput,
    ResetTasks,
  },
  data() {
    return {
      tasks: [
        "hoge",
        "hage",
      ]
    }
  },
  methods: {
    addTodo: function(newTask) {
      this.tasks = [
        ...this.tasks,
        newTask,
      ];
    },
    resetTasks: function() {
      this.tasks = [];
    },
  },
};
</script>

<style scoped>
#app {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin-top: 30px;
}
#todo-input {
  margin: 5px;
}
</style>

