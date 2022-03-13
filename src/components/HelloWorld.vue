<template>
  <div class="hello">
    <p>{{ msg }}</p>
    <p>{{ clickNum }}</p>
    <input type="button" value="Click!" v-on:click="onClick">
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },

  data(){
    return {
      clickNum: 0,
    }
  },

  methods: {
    onClick() {
      this.clickNum++;
      this.$emit("showClickNum", this.clickNum);
    },

  }
};

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
