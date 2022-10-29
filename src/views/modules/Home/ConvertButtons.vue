<template>
    <p>Convert text to...</p>
  <div class="btns">
      <button class="main-btn-secondary" @click="makeUppercase">UPPERCASE</button>
      <button class="main-btn-secondary" @click="makeLowercase">lowercase</button>
      <button class="main-btn-secondary" @click="makeSentencecase">
        Sentence case
      </button>
    <div class="last">
    </div>
  </div>
</template>

<script>
export default {
  name: "ConvertButtons",
  data() {
    return {};
  },
  methods: {
    makeUppercase() {
      var text = document.getElementById("textPlace");
      text.value = text.value.toUpperCase();
    },
    makeLowercase() {
      var text = document.getElementById("textPlace");
      text.value = text.value.toLowerCase();
    },
    makeSentencecase() {
      var text = document.getElementById("textPlace");
      text.value = text.value
        .toLowerCase()
        //eslint-disable-next-line
        .replace(/(^\s*\w|[\.\!\?]\s*\w)/g, function (c) {
          return c.toUpperCase();
        });
    },
  },
};
</script>

<style lang="scss" scoped>
button {
  padding: 1rem 4rem;
  border: none;
  border-radius: 10px;
  cursor: pointer;
  font-size: 1.2rem;
  font-weight: 500;
  margin-top: 1.5rem;
  min-width: 220px;
    transition: all ease 200ms;
    display: inline-block;
    margin: 0 1rem 1rem 0;
  &:hover {
    transform: translateY(-2px);
    transition: all ease 200ms;
    box-shadow: rgba(0, 0, 0, 0.1) 0px 4px 12px;
  }
}

.btns {
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
    &.last {
      button {
        margin-bottom: 0;
      }
    }
  @media (max-width: 991px) {
    margin-left: 0;
    button {
      width: 100%;
      margin-bottom: 1rem;
      margin-right: 0;
    }
  }
}
p {
  color: #596080;
  margin-bottom: 10px;
  margin-top: 38px;
  padding-bottom: 0.25rem;
}
</style>
