<template>
  <div id="click-box" v-on:click.exact="onClick" v-on:click.shift="onShiftClick">クリックしてください！</div>
  <p>内容: {{ description }}</p>
</template>


<script>
export default {
  name: "app",
  data: function() {
    return {
      description: "",
    };
  },
  methods: {
    onShiftClick: function() {
      this.description = "shift + click!";
    },
    onClick: function(e) {
      if (!e.shift) {
        this.description = "";
      }
    },
  },
};
</script>

<style scoped>
#click-box {
  width: auto;
  min-height: 20px;
  border: 2px solid blue;
}
</style>
