<template>
  <div class="container">
    <div><slot name="hoge" /></div>
    <div><slot /></div>
  </div>
</template>

<script>
export default {
}
</script>

<style scoped>
.container {
  display: flex;
  flex-direction: column;
}
</style>
