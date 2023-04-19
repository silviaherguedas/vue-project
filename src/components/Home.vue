<template>
  <div>{{ fullName }}</div>
  <button ref="btn">click!</button>
</template>

<script>
import { ref, toRefs, computed, inject, watch } from "vue";

export default {
  props: {
    firstName: String,
    lastName: String,
  },
  setup(props, { expose }) {
    const { firstName, lastName } = toRefs(props);

    const fullName = computed(() => {
      return `${firstName.value} ${lastName.value}`;
    });

    const btn = ref(null);
    console.log(btn.value); //* null

    expose({
      fullName,
    });

    watch(btn, (value) => {
      console.log(value); //* html
    });

    return {
      fullName,
      btn,
    };
  },
};
</script>
