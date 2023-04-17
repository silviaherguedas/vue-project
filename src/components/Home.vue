<script setup>
import { reactive } from "vue";
</script>

<script>
export default {
  setup() {
    const obj = reactive({ counter: 0 });
    setInterval(() => obj.counter++, 500);
    return {
      obj,
    };
  },
};
</script>

<template>
  <div>{{ obj.counter }}</div>
</template>
