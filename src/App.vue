<template>
  <div id="app">
    <get-joke-button></get-joke-button>
    <normal-joke-button></normal-joke-button>
    <loud-joke-button></loud-joke-button>
    <snake-joke-button></snake-joke-button>
    <display-joke></display-joke>
  </div>
</template>

<script>
//Import all components
import DisplayJoke from '@/components/DisplayJoke.vue'
import GetJokeButton from '@/components/GetJokeButton.vue'
import NormalJokeButton from '@/components/NormalJokeButton.vue'
import LoudJokeButton from '@/components/LoudJokeButton.vue'
import SnakeJokeButton from '@/components/SnakeJokeButton.vue'

export default {
  name: 'App',
  components: {
    DisplayJoke,
    GetJokeButton,
    NormalJokeButton,
    LoudJokeButton,
    SnakeJokeButton
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
