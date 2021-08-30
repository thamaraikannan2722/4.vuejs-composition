<template>
  <div>
    <input type="text" placeholder="First Name" v-model="firstName" />
    <input type="text" placeholder="Last Name" v-model="lastName" />
  </div>

  <PersonGreeting :firstName="firstName" :lastName="lastName" @callHeroes="callHeroes" />
</template>

<script>
//63.Props and Composition API -
//64.Custom Events and Composition API -

import { ref } from "vue";
import PersonGreeting from "../38.Props and Composition API/PersonGreeting";

export default {
  name: "Person",
  components: {PersonGreeting},
  setup() {
    const firstName = ref("");
    const lastName = ref("");

    function callHeroes(hero) {
        alert(`Calling ${hero}`)
    }

    return {
      firstName,
      lastName,
      callHeroes,
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
