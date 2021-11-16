<template>
  <header class="ly-header">
    <h1>Case convert</h1>
    <p>Convert upper case to lower case, lower case ...</p>
  </header>
</template>

<script>
export default {
  name: "Header",
  data() {
    return {};
  },
};
</script>

<style lang="scss" scoped>
.ly-header {
  padding: 1rem 0;
  text-align: center;
  h1 {
    font-size: 2.5rem;
  color: $c-secondary-400;
  }
  p {
    font-size: 1rem;
  }
}
</style>
