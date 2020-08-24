<template>
  <div id="app">
    <customHeader title="les apprenants de la KDA" />
    <customSection />
  </div>
</template>

<script>
import Header from "./components/header";
import Section from "./components/section";
export default {
  name: "App",
  components: {
    customHeader: Header,
    customSection: Section,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
</style>
