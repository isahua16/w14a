<template>
  <div id="app">
    <get-joke></get-joke>
    <loud-joke></loud-joke>
    <display-joke></display-joke>
  </div>
</template>

<script>
import DisplayJoke from '@/components/DisplayJoke.vue'
import GetJoke from '@/components/GetJokeButton.vue'
import LoudJoke from '@/components/LoudJokeButton.vue'

export default {
  name: 'App',
  components: {
    DisplayJoke,
    GetJoke,
    LoudJoke

  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
