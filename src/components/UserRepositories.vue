<template>
  <h1>{{ user }} Repositories</h1>
  <p>{{ total }}</p>
</template>

<script>
export default {
  props: {
    user: {
      type: String,
      required: true,
    },
    repositories: {
      type: Number,
      default: 100,
    },
  },
  data() {
    return {
      filters: {}, // 3
      searchQuery: "", // 2
    };
  },
  setup(props, ctx) {
    console.log("props", props);
    console.log("ctx", ctx);

    const total = `Total ${props.repositories}`;
    return {
      total,
    };
  },
  computed: {
    filteredRepositories() {
      // 3
      return null;
    },
    repositoriesMatchingSearchQuery() {
      // 2
      return null;
    },
  },
};
</script>
