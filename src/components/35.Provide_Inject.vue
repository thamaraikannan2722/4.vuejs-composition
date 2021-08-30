<template>
  <h3>Parent Component {{ name }}</h3>

  <h3>Parent Component Count {{ count }}</h3>
  <h3>Parent Component Hero {{ firstName }} {{ lastName }}</h3>

  <button @click="incrementCount">Increment Count from Parent</button>
  <ChildA />
</template>

<script>
//60.Replacing Provide Inject -

import { provide, ref, reactive, toRefs } from "vue";

import ChildA from "../../35.Provide Inject/ChildA";

export default {
  name: "ProvideInject",
  components: {
    ChildA,
  },
  setup() {
    provide("c_userName", "AM Studios");

    const count = ref(0);
    function incrementCount() {
      count.value++;
    }

    const state = reactive({
      firstName: "Bruce",
      lastName: "Wayne",
    });

    provide("c_count", count);
    provide("c_hero", state);
    provide("incrementCount", incrementCount);

    return {
      count,
      ...toRefs(state),
      incrementCount,
    };
  },
  data() {
    return {
      name: "Ashwin",
    };
  },
  provide() {
    return {
      userName: this.name,
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
