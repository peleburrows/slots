<template>
  <div id="app">
      <h1>App.vue</h1>
    <Component-A>
        <template v-slot:default="slotProps">
            <p>Using data from parent slot (App.vue): <strong>{{ user.firstName }}</strong></p>
            <p>Using data from slot (ComponentA.vue): <strong>{{ slotProps.user.firstName }}</strong></p>

            <!-- <button @click="clickMethod">
                Click me and watch console
            </button> -->
        </template>
        <template v-slot:age="otherSlotProps">
            <p>Using data from parent slot (App.vue): <strong>{{ user.age_months }}</strong></p>
            <p>Using data from slot (ComponentA.vue): <strong>{{ otherSlotProps.user.age_years }}</strong></p>
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
              age_years: 50,
              age_months: 620,
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
