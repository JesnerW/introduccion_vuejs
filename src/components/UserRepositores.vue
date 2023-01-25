<template>
  <div>{{ user }} Repositories</div>
</template>

<script>
import { type } from "os";

export default {
  props: {
    user: {
      type: String,
      require: true,
    },
  },
  setup(props, ctx) {
    return {
      // repositores,
    };
  },
  data() {
    return {
      repositores: [],
      filters: {},
      searchQuery: "",
    };
  },
  computed: {
    filteredRepositories() {
      return null;
    },
    repositoriesMatchingSearchQuery() {
      return null;
    },
  },
};
</script>
