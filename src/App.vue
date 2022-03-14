<template>
  <div>
    <div class="container">
      <HelloWorld>
        hogehoge
      </HelloWorld>
      <transition>
        <span class="box" v-if="show" ></span>
      </transition>
    </div>
    <button @click="show = !show">fade</button>
  </div>
</template>

<style>
.container{
  height: 100px;
}
.box {
  display: block;
  width: 50px;
  height: 50px;
  background: #000;
}

button{
  display: block;
}

/* アニメーション処理 */
.v-leave-active,
.v-enter-active {
  transition: opacity 1s;
}
.v-enter-from,
.v-leave-to {
  opacity: 0;
}
</style>

<script>
import HelloWorld from "./components/HelloWorld.vue";


export default {
  components: {
    HelloWorld,
  },
  data: function() {
    return {
      show: true
    };
  }
};
</script>
