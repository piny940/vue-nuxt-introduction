<template>
  <div>
    <input type="text" name="" id="" placeholder="タスクを入力してください。" v-model="input">
    <input type="button" value="追加" v-on:click="onClick">
  </div>
</template>

<script>
export default {
  data() {
    return {
      input: "",
    };
  },
  props: {
    addTodo: Function,
  },
  methods: {
    onClick: function() {
      this.addTodo(this.input);
      this.input = "";
    },
  },
};
</script>
