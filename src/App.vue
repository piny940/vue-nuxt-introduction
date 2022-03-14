<script>
import HelloWorld from "./components/HelloWorld.vue";

export default {
  name: "app",
  components: {
    HelloWorld,
  },
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
  render: function() {
    return (
      <>
        <div id="click-box" onclick={this.onClick}>クリックしてください！</div>
        <p>内容: { this.description }</p>
        <HelloWorld message="hage">
          hogehoge
        </HelloWorld>
      </>
    );
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
