<script setup>
import { ref } from "vue";
</script>

<script>
export default {
  setup() {
    const text = ref("hola Vue");
    console.log(text.value);

    const count = ref(0);
    setInterval(() => count.value++, 500);

    return {
      text,
      count,
    };
  },
};
</script>

<template>
  <div>{{ text }}</div>
  <div>Contador: {{ count }}</div>
</template>
