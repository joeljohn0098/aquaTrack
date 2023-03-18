<template >
  <div id="app">
    <!-- <nav>
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </nav>
    <router-view/> -->
    <IndexView />
  </div>
</template>

<script>
import IndexView from '@/views/IndexView.vue'

export default {
  name: 'HomeView',
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
  background-color: yellowgreen;
}

nav {
  padding: 30px;
}
</style>
