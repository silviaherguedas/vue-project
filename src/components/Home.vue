<script setup>
import { inject, onMounted, ref } from "vue";

const { firstName, lastName } = inject("objPerson");

//accede al elemento [h1]
const elem = ref(null);
onMounted(() => console.log("elem:", elem.value));
</script>

<template>
  <h1 ref="elem">Full Name: {{ firstName + " " + lastName }}</h1>
</template>
