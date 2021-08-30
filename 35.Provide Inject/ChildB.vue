<template>
  <h3>Child Component B</h3>
  <ChildC />
</template>

<script>
//60.Replacing Provide Inject -

import ChildC from "../35.Provide Inject/ChildC";

export default {
  name: "ChildB",
  components: {
    ChildC,
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
