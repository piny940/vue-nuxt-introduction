<template>
  <HelloWorld msg="Welcome to Your Vue.js App" v-on:showClickNum="showClickNum"/>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    HelloWorld
  },

  data() {
    return {
      message: "",
    };
  },
  methods: {
    showClickNum(num) {
      window.alert(num);
    }
  },
};
</script>

<style>

</style>
