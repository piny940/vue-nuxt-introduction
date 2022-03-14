<template>
  <div>
    <div class="container">
      <HelloWorld>
        hogehoge
      </HelloWorld>
      <transition
        v-on:after-enter="afterEnter"
        v-on:before-enter="beforeEnter"
        v-on:enter="onEnter"
        v-on:after-leave="afterLeave">
        <span class="box" v-if="show" ></span>
      </transition>
    </div>
    <button @click="show = !show">fade</button>
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";


export default {
  components: {
    HelloWorld,
  },
  data: function() {
    return {
      show: true,
      hasEntered: true,
    };
  },
  methods: {
    afterEnter: function() {
      console.log("hasEntered!");
    },
    onEnter: function() {
      console.log("onEnter");
    },
    beforeEnter: function() {
      console.log("before enter");
    },
    afterLeave: function() {
      console.log("after leave");
    },
  },
};
</script>

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
  transition: all 1s ease-out;
}
.v-enter-from,
.v-leave-to {
  opacity: 0;
  transform: translateX(200px) rotateZ(360deg) rotateX(180deg);
}
</style>
