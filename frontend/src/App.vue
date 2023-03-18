<template >
  <div id="app">
    <IndexView />
  </div>
</template>

<script>
import IndexView from '@/views/IndexView.vue'

export default {
  name: 'Home',
  components: {
    IndexView
  }
}

</script>


<style>
#app {
  font-family: 'Courier New', monospace;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
</style>
