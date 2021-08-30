<template>
  <h2>{{ name }}</h2>
  <button @click="setName">Change Name</button>

  <h2>{{ count }}</h2>
  <button @click="incrementCount">Increment Count</button>

  <h2>{{ first }} {{ last }}</h2>
  <button @click="changeHero">Change Hero</button>
</template>

<script>
//55.Replacing Methods -

import { ref, reactive, toRefs } from "vue";

export default {
  name: "Methods",
  setup() {
    const count = ref(0);
    const state = reactive({
      first: "Bruce",
      last: "Wayne",
    });

    function incrementCount() {
      count.value++;
    }

    function changeHero() {
      (state.first = "Clark"), (state.last = "Kent");
    }

    return {
      count,
      incrementCount,
      ...toRefs(state),
      changeHero,
    };
  },
  data() {
    return {
      name: "Ashwin",
    };
  },
  methods: {
    setName() {
      this.name = "AM Studios";
    },
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
