<template>
  <div id="app">
    <Signal msg="Hello World!" />
  </div>
</template>

<script>
import Signal from './components/Signal.vue'

export default {
  name: 'app',
  components: {
    Signal
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.marine-signal {
  font-size: 2rem;
}
</style>
