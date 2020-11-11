<template>
  <div id="app">
      <Home/>
  </div>
</template>

<script>
import Home from './components/home'

export default {
  name: 'App',
  components: {
      Home
  }
}
</script>

<style>
#app {
    height: 100%;
    background-color: #324152;
}
</style>
