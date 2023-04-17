<script setup>
import base from "@/mixins/base";
</script>

<script>
export default {
  name: "App",
  mixins: [base],
  data() {
    return {
      text: "Hola Vue",
    };
  },
  beforeCreate() {
    console.log("beforeCreate", this.$data, this.$el);
  },
  created() {
    console.log("created", this.$data, this.$el);
  },
  mounted() {
    console.log("mounted", this.$data, this.$el);
  },
};
</script>

<template>
  <div>
    {{ text }}
  </div>
  <div>
    {{ algo }}
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
