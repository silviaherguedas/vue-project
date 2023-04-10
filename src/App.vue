<script setup>
import Modal from "./components/Modal.vue";
</script>

<script>
export default {
  name: "App",
  components: {
    Modal,
  },
};
</script>

<template>
  <div>
    <Modal />
  </div>
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
