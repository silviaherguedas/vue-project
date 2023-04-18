<template>
  <div>{{ fullName }}</div>
</template>

<!-- <script setup>
import { useAttrs } from "vue";

const attrs = useAttrs();
console.log(attrs);

</script> -->

<script>
import { toRefs, computed } from "vue";

export default {
  props: {
    firstName: String,
    lastName: String,
  },
  setup(props, { attrs, slots, emit, expose }) {
    console.log(attrs);
    console.log(slots);
    console.log(emit);
    console.log(expose);

    const { firstName, lastName } = toRefs(props);

    const fullName = computed(() => {
      return `${firstName.value} ${lastName.value}`;
    });

    expose({
      fullName,
    });

    return {
      fullName,
    };
  },
};
</script>
