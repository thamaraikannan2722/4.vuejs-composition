<template>
  
<Data />
<DemoOne />
<DemoTwo />
<Methods />
<VModel />
<Computed />
<Watch />
<ProvideInject />
<LifecycleO />
<LifecycleC />
<TemplateRef />
<Person />
<ClickCounter />
<HoverCounter />

</template>

<script>

import Data from "../src/components/29.Replacing_data_with_Ref";
import DemoOne from "../src/components/30.Reactivity_and_toRefs";
import DemoTwo from "../src/components/30.Reactivity_and_toRefs_1";
import Methods from "../src/components/31.Replacing_Methods";
import VModel from "../src/components/32.V-model_and_Composition_API";
import Computed from "../src/components/33.Replacing_Computed_Properties";
import Watch from "../src/components/34.Replacing_Watchers";
import ProvideInject from "../src/components/35.Provide_Inject";
import LifecycleO from "../36.Replacing Lifecycle Hooks/LifecycleO";
import LifecycleC from "../36.Replacing Lifecycle Hooks/LifecycleC";
import TemplateRef from "../src/components/37.Template_Refs";
import Person from "../38.Props and Composition API/Person";
import ClickCounter from "../39.Resuability with Composition API/ClickCounter";
import HoverCounter from "../39.Resuability with Composition API/HoverCounter";

export default {
  name: 'App',
  components: {
    Data,
    DemoOne,
    DemoTwo,
    Methods,
    VModel,
    Computed,
    Watch,
    ProvideInject,
    LifecycleO,
    LifecycleC,
    TemplateRef,
    Person,
    ClickCounter,
    HoverCounter,
  }
}
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
