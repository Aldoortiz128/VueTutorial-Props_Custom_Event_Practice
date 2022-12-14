<template>
  <section>
    <!--Rendering prop values with interpolation -->
    <h2>{{ username }}</h2>
    <h3>{{ userage }}</h3>
  </section>
</template>

<script>
export default {
  //Props being passed to the main app
  props: {
    username: {
      type: String,
      required: true
    },
    userage: {
      type: Number,
      required: true
    },
  },
  methods: {},
};
</script>
<style>
</style>

