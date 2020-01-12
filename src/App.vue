<template>
  <div id="app">
      <h1>App.vue</h1>
    <Component-A/>
  </div>
</template>

<script>
import ComponentA from './components/ComponentA.vue'

export default {
  name: 'app',
  components: {
    ComponentA
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
  background-color: #95a5a6;
  padding: 50px;
}
</style>
