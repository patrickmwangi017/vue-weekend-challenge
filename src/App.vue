<template>
  <div id="app" class="min-h-screen w-full bg-gray-200">
    <main>
      <component
        v-for="(component, index) in page.components"
        :key="index"
        :is="component.name"
        v-bind="component.props"
      />
    </main>
  </div>
</template>

<script>
import About from "./components/About";
import Milestones from "./components/Milestones";
import WhatWeDo from "./components/WhatWeDo";
import Header from "./components/Header";
export default {
  name: "App",
  components: {
    About,
    Milestones,
    WhatWeDo,
    Header
  },
  data() {
    return {
      page: {
        components: [
          {
            name: "Header",
            props: {}
          },
          {
            name: "WhatWeDo",
            props: {}
          },
          {
            name: "About",
            props: {}
          },
          {
            name: "Milestones",
            props: {}
          }
          
        ]
      }
    };
  }
};
</script>

<style>
</style>
