<template>
<div class="w-100">
    <p>1. Place your text</p>
  <textarea
  v-on:keyup="this.$data.name = $event.target.value"
    id="textPlace"
    name=""
    cols="30"
    rows="10"
    placeholder="Place your text here..."
  ></textarea><button v-on:click="getName">getName</button>
  </div>
</template>

<script>
export default {
  name: "Home",
  components: {},
  data() {
    return {
    };
  },
  methods: {
    getName: function () {
      alert(this.name);
    }
  }
};
</script>

<style lang="scss" scoped>
    #textPlace{
      width: 100%;
      padding: 1rem;
        border: 2px solid $c-secondary-500;
    }
    p {
      color: $c-primary-900;
      margin-bottom: 0;
      padding-bottom: .25rem;
    }
</style>
