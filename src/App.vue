<template>
  <div id="app">
      <h1>App.vue</h1>
    <Component-A>
        <template v-slot:default="{defaultSlotProps, clickMethod}">
            {{ user.firstName }}

            <button @click="clickMethod">
                Click me and watch console
            </button>
        </template>
        <template v-slot:age="otherSlotProps">
            {{ user.age }}
        </template>
    </Component-A>
  </div>
</template>

<script>
import ComponentA from './components/ComponentA.vue'

export default {
  name: 'app',
  components: {
    ComponentA
  },
  data() {
      return {
          user: {
              firstName: 'Nicholas',
              lastName: 'Cage',
              age: 50,
          }
      };
  },
    methods: {
      clickMethod() {
          console.log('method click in App.vue');
      }
  },
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
