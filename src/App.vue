<template>
  <div id="app">
    <Player/>
  </div>
</template>

<script>
import Player from './components/Player.vue'

export default {
  name: 'App',
  components: {
    Player
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Oswald&display=swap');
body
{
  margin: 0;
  padding: 0;
}
#app {
  font-family: 'Oswald', Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  font-size: 1rem;
  color: #333333;
}
</style>
