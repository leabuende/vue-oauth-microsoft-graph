<template>
  <div id="app">
    <baselayout>
      <homepage />
    </baselayout>
  </div>
</template>

<script>
import homepage from "./components/HomePage.vue";
import baselayout from "./components/baselayout.vue";

export default {
  name: "App",
  components: {
    homepage,
    baselayout,
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
}
</style>
