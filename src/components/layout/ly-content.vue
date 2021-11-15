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
  .ly-content{
    min-width: 900px;
    margin: 0 auto;
    @media(max-width: 991px){
      min-width: unset;
    }
  }
</style>
