<template>
  <div class="componentA">
      <h2>Component A</h2>

        <slot v-bind:user="user" :clickMethod="clickMethod">
            {{ user.lastName }}
        </slot>


        <slot v-bind:user="user"
              name="age"
        >
            {{ user.age }}
        </slot>

        <slot name="fictional">
            {{ user.fictional }}
        </slot>


      <Component-B>
          
      </Component-B>
  </div>
</template>

<script>

import ComponentB from './ComponentB.vue'

export default {
  name: 'Component-A',
  components: {ComponentB},
  props: {},
  data() {
      return {
          user: {
              firstName: 'Don',
              lastName: 'Quixote',
              age: 219,
              fictional: 'yeah totally made up',
          }
      };
  },
  methods: {
      clickMethod() {
          console.log('method click in ComponentA');
      }
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
    .componentA {
        padding: 50px;
        background-color: #1abc9c;
    }
</style>
