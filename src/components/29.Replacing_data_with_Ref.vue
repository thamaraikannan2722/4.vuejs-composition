<template>

  <h2>Options - {{ o_firstName }}</h2>
  <h2>Composition - {{ c_firstName }}</h2>
  <h2>Composition - {{ greet }}</h2>

  <h2>Options - {{ o_firstName }} {{ o_lastName }} a.k.a {{ o_heroName }}</h2>
  <h2>Composition - {{ c_firstName }} {{ c_lastName }} {{ c_heroName }}</h2>
  <h2>Composition - {{ greetHero }}</h2>

  <h2>
    Composition - {{ state.firstName }} {{ state.lastName }}
    {{ state.heroName }}
  </h2>
  <h2>Composition - {{ reactiveGreetHero }}</h2>
</template>

<script>
//52.Replacing Data with Ref(composition api) -
//53.Replacing Data with Reactive -

import { ref, reactive } from "vue";

export default {
  name: "Data",
  setup() {
    const c_firstName = ref("Clark");
    //c_firstName.value = 'Diana';
    const greet = `Hello ${c_firstName.value}`;
    console.log("c_firstName", c_firstName);

    const c_lastName = ref("Kent");
    const c_heroName = ref("Superman");
    const greetHero = `Hello ${c_firstName.value} ${c_lastName.value} a.k.a ${c_heroName.value}`;

    const state = reactive({
      firstName: "Princess",
      lastName: "Diana",
      heroName: "Wonder Women",
    });

    const reactiveGreetHero = `Hello ${state.firstName} ${state.lastName} a.k.a ${state.heroName}`;

    const isLoggedIn = ref(false);
    const isLoggedInReactive = reactive({
      value: false,
    });

    return {
      c_firstName,
      greet,

      c_lastName,
      c_heroName,
      greetHero,
      state,
      reactiveGreetHero,

      isLoggedIn,
      isLoggedInReactive,
    };
  },
  data() {
    return {
      o_firstName: "Bruce",
      o_lastName: "Wayne",
      o_heroName: "Batman",
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
