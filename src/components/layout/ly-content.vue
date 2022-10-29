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
    width: 100%;
    margin: 0 auto;
    max-width: 1199px;
    @media(max-width: 991px){
      min-width: unset;
    }
  }
</style>
