<template>
  <div class="wrapper">
    <static></static>
    <nearby></nearby>
  </div>
  <docker></docker>
</template>

<script>
import Static from './Static.vue'
import Nearby from './Nearby.vue'
import Docker from './Docker.vue'

export default {
  name: 'Home',
  components: {
    Static,
    Nearby,
    Docker
  }
}
</script>

<style lang="scss">
  // 顶部
  .wrapper {
    overflow-y: auto;
    position: absolute;
    left: 0;
    right: 0;
    top: 0;
    bottom: .5rem;
    padding: 0 .18rem .15rem .18rem;
  }
</style>
