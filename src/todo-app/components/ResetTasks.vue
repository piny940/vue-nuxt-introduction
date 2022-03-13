<template>
  <input type="button" value="タスクをリセット" v-on:click="resetTasks">
</template>

<script>
export default {
  props: {
    resetTasks: {
      type: Function,
      required: true,
    },
  },
};
</script>
