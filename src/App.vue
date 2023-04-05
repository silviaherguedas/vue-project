<script setup>
import Menu from "./components/Menu.vue";
</script>

<script>
export default {
  name: "App",
  // components: { Menu },
  data() {
    return {
      show: false,
    };
  },
};
</script>

<template>
  <button @click="show = !show">Menu</button>
  <transition name="fade">
    <Menu v-show="show"></Menu>
  </transition>
</template>

<style scoped>
.fade-leave-to,
.fade-enter-to {
  opacity: 0;
}

.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.5s ease;
}
</style>
