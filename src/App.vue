<script setup>
import HelloWorld from "./components/HelloWorld.vue";
import TheWelcome from "./components/TheWelcome.vue";
</script>

<script>
export default {
  name: "App",
  components: {
    HelloWorld,
  },
  data() {
    return {
      componente_dinamico: "HelloWorld",
    };
  },
};
</script>

<template>
  <header>
    <img
      alt="Vue logo"
      class="logo"
      src="./assets/logo.svg"
      width="125"
      height="125"
    />

    <div class="wrapper">
      // componente dinámico con sus props
      <component
        :is="componente_dinamico"
        v-bind="{ msg: 'Hola Vue' }"
      ></component>

      // otro ejemplo
      <component
        :is="HelloWorld"
        msg="mensaje de prueba"
        titlecustom="This a fucking vuejs"
      ></component>
    </div>
  </header>

  <main>
    <TheWelcome />
  </main>
</template>

<style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
