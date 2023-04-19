<script setup>
import Home from "./components/Home.vue";
import { provide, reactive } from "vue";

const persona = reactive({
  firstName: "Pepe",
  lastName: "Argento",
});

provide("objPerson", persona);
</script>

<template>
  <Home />
</template>
