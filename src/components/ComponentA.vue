<template>
  <div class="componentA">
      <h2>Component A</h2>
      <Component-B/>
  </div>
</template>

<script>

import ComponentB from './ComponentB.vue'

export default {
  name: 'Component-A',
  components: {ComponentB},
  props: {}
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
    .componentA {
        padding: 50px;
        background-color: #1abc9c;
    }
</style>
