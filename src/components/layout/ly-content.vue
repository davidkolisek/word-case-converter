<template>
  <main class="ly-content">
    <slot/>
  </main>
</template>

<script>
export default {
  name: "Content",
  props: {
    title: String,
    subtitle: String,
  },
};
</script>

<style lang="scss" scoped>

</style>
