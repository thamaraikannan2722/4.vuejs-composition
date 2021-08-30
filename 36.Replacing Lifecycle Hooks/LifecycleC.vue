<template>
  <div>Composition API Lifecycle Hooks</div>
</template>

<script>
//61.Replacing Lifecycle Hooks -

import {
  onBeforeMount,
  onMounted,
  onBeforeUpdate,
  onUpdated,
  onBeforeUnmount,
  onUnmounted,
} from "vue";
export default {
  name: "LifecycleC",
  setup() {
    onBeforeMount(() => {
      console.log("LifeCycleC onBeforeMount()");
    });
    onMounted(() => {
      console.log("LifeCycleC onMounted()");
    });
    onBeforeUpdate(() => {
      console.log("LifeCycleC onBeforeUpdate()");
    });
    onUpdated(() => {
      console.log("LifeCycleC onUpdated()");
    });
    onBeforeUnmount(() => {
      console.log("LifeCycleC onBeforeUnmount()");
    });
    onUnmounted(() => {
      console.log("LifeCycleC onUnmounted()");
    });
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
