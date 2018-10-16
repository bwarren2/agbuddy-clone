<template>
  <div id="app">
  <ScoreScreen/>
  </div>
</template>

<script>
import ScoreScreen from './components/ScoreScreen.vue'

export default {
  name: 'app',
  components: {
    ScoreScreen
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
</style>
