<template>
  <div>
    <h2 @mouseover="incrementCount">Hovered {{ count }} times</h2>
  </div>
</template>

<script>
//65.Resuability with Composition API -

// import CounterMixin from "../src/mixins/counter.js"
import useCounter from "../src/composables/useCounter.js";

export default {
  name: "HoverCounter",
  setup() {
    const { count, incrementCount } = useCounter();
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
