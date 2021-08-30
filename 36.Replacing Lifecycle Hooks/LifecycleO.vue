<template>
  <div>Options API Lifecycle Hooks</div>
</template>

<script>
//61.Replacing Lifecycle Hooks -

export default {
  name: "LifecycleO",
  beforeCreate() {
    console.log("LifeCycleO beforeCreate()");
  },
  created() {
    console.log("LifeCycleO created()");
  },
  beforeMount() {
    console.log("LifeCycleO beforeMount()");
  },
  mounted() {
    console.log("LifeCycleO mounted()");
  },
  beforeUpdate() {
    console.log("LifeCycleO beforeUpdate()");
  },
  updated() {
    console.log("LifeCycleO updated()");
  },
  beforeUnmount() {
    console.log("LifeCycleO beforeUnmount()");
  },
  unmounted() {
    console.log("LifeCycleO unmounted()");
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
