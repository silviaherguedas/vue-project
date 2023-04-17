<script setup>
import Home from "./components/Home.vue";
</script>

<script>
export default {
  name: "App",
  components: {
    Home,
  },
};
</script>

<template>
  <Home></Home>
</template>

<style scoped>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
