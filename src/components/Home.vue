<template>
  {{ fullName }}
</template>

<script setup>
import { computed, toRefs, watch } from "vue";

const props = defineProps({
  firstName: String,
  lastName: String,
});

const { firstName, lastName } = toRefs(props);

const fullName = computed(() => {
  return `${firstName.value} ${lastName.value}`;
});

watch(firstName, (newValue, oldValue) => {
  console.log(`The new name is ${newValue}`);
  console.log(`The old name is ${oldValue}`);
});
</script>
