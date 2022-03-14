<script>
export default {
  render: function() {
    return (
      <div>
        {this.$slots.default()}
      </div>
    );
  },
};
</script>
