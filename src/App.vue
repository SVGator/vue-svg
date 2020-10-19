<template>
  <div id="app">
    <HelloSvg />
  </div>
</template>

<script>
import HelloSvg from "./components/HelloSvg.vue";

export default {
  name: "App",
  components: {
    HelloSvg,
  },
};
</script>

<style>
body {
  margin: 0;
  padding: 0;
  border: 0;
  overflow: hidden;
}
</style>
