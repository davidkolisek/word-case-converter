<template>
  <div class="btns">
    <p>2. Click to convert</p>
    <div>
      <button class="main-btn-primary" @click="makeUppercase">UPPERCASE</button>
    </div>
    <div>
      <button class="main-btn-primary" @click="makeLowercase">lowercase</button>
    </div>
    <div>
      <button class="main-btn-primary" @click="makeSentencecase">
        Sentence case
      </button>
    </div>
    <div class="last">
      <button class="main-btn-secondary" @click="copyToClipboard">
        <i class="icon-copy"></i>Copy!
      </button>
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
    copyToClipboard() {
      var aux = document.createElement("input");
      aux.setAttribute("value", document.querySelector("#textPlace").value);
      document.body.appendChild(aux);
      aux.select();
      document.execCommand("copy");
      document.body.removeChild(aux);
      document.querySelector(".copied-popup").classList.add("active");
      setTimeout(function () {
        document.querySelector(".copied-popup").classList.remove("active");
      }, 3000);
    },
  },
};
</script>

<style lang="scss" scoped>
button {
  padding: 0.75rem 2.5rem;
  border: none;
  border-radius: 5px;
  cursor: pointer;
  font-size: 1.1rem;
  font-weight: 500;
  margin-bottom: 1.5rem;
  min-width: 220px;
}

.btns {
  display: flex;
  flex-direction: column;
  margin-left: 2rem;
  div {
    &.last {
      button {
        margin-bottom: 0;
      }
    }
  }
  @media (max-width: 991px) {
    margin-top: 2rem;
    margin-left: 0;
    button {
      width: 100%;
      margin-bottom: 1rem;
    }
  }
}
p {
  color: $c-primary-900;
  margin-bottom: 0;
  padding-bottom: 0.25rem;
}
</style>
