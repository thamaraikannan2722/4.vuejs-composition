<template>
  <div>Hello {{ firstName }} {{ lastName }}</div>

  <div>Hello {{ fullName }}</div>

  <button @click="sendEvent">Call Heroes</button>
</template>

<script>

//63.Props and Composition API - 
//64.Custom Events and Composition API -

import { computed } from 'vue'

export default {
  name: "PersonGreeting",
  props: ['firstName', 'lastName'],
  emits: ['callHeroes'],
  setup (props, context) {
      console.log(context)
      const fullName = computed(() => {
          return `${props.firstName} ${props.lastName}`
      })

      function sendEvent() {
          context.emit('callHeroes', fullName.value)
      }

      return {
          fullName,
          sendEvent,
      }
  },
//   computed: {
//       fullName() {
//           return `${this.firstName} ${this.lastName}`
//       }
//   },
  data() {
    return {
    };
  },
};
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