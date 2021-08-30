<template>
  <div>
    <h2>{{ firstName }} {{ lastName }}</h2>
    <h2>{{ fName }} {{ lName }}</h2>
  </div>
</template>

<script>
//54.Reactivity and toRefs - setTimeOut(() => {})

import { reactive, toRefs } from "vue";

export default {
  name: "DemoTwo",
  setup() {
    const state = reactive({
      firstName: "Bruce",
      lastName: "Wayne",
    });

    setTimeout(() => {
      state.firstName = 'Clark';
      state.lastName = 'Kent';
      console.log(state);
    }, 2000);

    return toRefs(state)
  },
  data() {
    return {
      fName: 'Bruce',
      lName: 'Wayne',
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
