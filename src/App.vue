<script setup>
import Home from "./components/Home.vue";
import { ref, provide } from "vue";
</script>

<script>
export default {
  name: "App",
  components: {
    Home,
  },
  setup() {
    const username = ref("DianaNerd");
    provide("username", username);
  },
};
</script>

<template>
  <Home first-name="Silvia" last-name="Herguedas"></Home>
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
