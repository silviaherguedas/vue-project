<script setup>
import onMounted from "vue";
</script>

<script>
export default {
  setup() {
    onMounted(() => {
      console.log("mounted!");
    });
  },
};
</script>

<template>
  <div>Hola</div>
</template>
