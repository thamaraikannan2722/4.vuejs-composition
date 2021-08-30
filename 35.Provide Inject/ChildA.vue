<template>
  <h3>Child Component A</h3>
  <ChildB />
</template>

<script>
//60.Replacing Provide Inject -

import ChildB from "../35.Provide Inject/ChildB";

export default {
  name: "ChildA",
  components: {
    ChildB,
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
