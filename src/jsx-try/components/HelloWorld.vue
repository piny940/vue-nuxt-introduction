<script>
export default {
  props: {
    message: {
      type: String,
      required: true,
    },
  },

  render: function() {
    return (
      <div class="container">
        <div><slot name="hoge" /></div>
        <div>{this.$slots.default()}hoge</div>
        <div>{this.message}</div>
      </div>
    )
  },
}
</script>

<style scoped>
.container {
  display: flex;
  flex-direction: column;
}
</style>
