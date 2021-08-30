<template>
  <div>
    <input type="text" ref="inputRef" />
  </div>
</template>

<script>
//62.Template Refs and Composition API -

import { ref, onMounted } from "vue";

export default {
  name: "TemplateRef",
  setup() {
    const inputRef = ref(null);

    onMounted(() => {
      inputRef.value.focus();
    });

    return {
      inputRef,
    };
  },
//   mounted() {
//     this.$refs.inputRef.focus();
//   },
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
