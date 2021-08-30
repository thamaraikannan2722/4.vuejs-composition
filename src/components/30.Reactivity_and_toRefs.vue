<template>
  <div>
    <h2>{{ name }}</h2>
  </div>
</template>

<script>

//54.Reactivity and toRefs - setTimeOut(() => {})

import { ref } from 'vue'

export default {
  name: "DemoOne",
  setup() {
    const name = ref("Ashwin");

    setTimeout(() => {
        name.value = 'AM Studios';
        console.log(name);
    },2000)

    return {
      name,
    };
  },
  data() {
    return {};
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
