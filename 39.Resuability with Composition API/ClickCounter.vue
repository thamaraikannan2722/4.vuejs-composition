<template>
  <div>
    <button @click="incrementCount">Clicked {{ count }} times</button>
  </div>
</template>

<script>
//65.Resuability with Composition API -

// import CounterMixin from "../src/mixins/counter.js";
import useCounter from "../src/composables/useCounter.js";

export default {
  name: "ClickCounter",
  setup() {
    const { count, incrementCount } = useCounter(100, 10);
    return {
      count,
      incrementCount,
    };
  },
  // mixins: [CounterMixin],
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
