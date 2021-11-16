<template>
<div class="w-100">
    <p>1. Place your text</p>
    <div class="area">
  <textarea
    v-on:keyup="getVal"
    id="textPlace"
    name=""
    cols="30"
    rows="10"
    placeholder="Place your text here..."
  ></textarea>
  <!-- <button v-on:click="getName">getName</button> -->
  <p class="other-info"> <span> Characters: <strong id="charCount"></strong></span><span>Words: <strong id="wordCount"></strong></span><span>Sentences: <strong id="sentenceCount"></strong></span></p>
  </div>
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
    getVal: function () {
      document.getElementById("charCount").innerHTML = document.getElementById("textPlace").value.length;
      document.getElementById("wordCount").innerHTML = document.getElementById("textPlace").value.trim().split(/\s+/).length;
      document.getElementById("sentenceCount").innerHTML = document.getElementById("textPlace").value.split(/[.!?]+\s/).filter(Boolean).length;
    }
  }
};
</script>

<style lang="scss" scoped>
.area{
}

.other-info {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
}
    #textPlace{
      width: 100%;
      padding: 1rem;
        border: 2px solid $c-secondary-500;
    }
    p {
      color: $c-primary-900;
      margin-bottom: 0;
      padding-bottom: .25rem;
      span {
        display: inline-block;
      color: #ccc;
          margin-right: .5rem;
        &:last-child{
          margin-right: 0;
        }
      }
    }
</style>
