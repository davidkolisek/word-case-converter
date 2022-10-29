<template>
<div class="w-100">
    <div class="area">
  <textarea
    v-on:keyup="getVal"
    id="textPlace"
    name=""
    cols="30"
    rows="10"
    placeholder="Place your text here..."
    autofocus
  ></textarea>
  <!-- <button v-on:click="getName">getName</button> -->
  <p class="other-info"> 
      <span> Characters: <strong id="charCount">0</strong></span>
      <span>Words: <strong id="wordCount">0</strong></span>
      <span>Sentences: <strong id="sentenceCount">0</strong></span>
      <button class="main-btn-secondary" @click="copyToClipboard">
        <i class="icon-copy"></i>Copy!
      </button>
      </p>
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
  }
};
</script>

<style lang="scss" scoped>
.area{
  border: 1px solid #EBEDF5;
        border-radius: 20px;
        box-shadow: rgba(17, 12, 46, 0.15) 0px 48px 100px 0px;
        background: #fff;
        overflow: hidden;
        .h5 {
          padding: 1.5rem ;
  background: #fcfcfc;
        }
        .other-info {

          padding: 1.5rem 1.5rem ;
        }

}

.other-info {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
  background: #fcfcfc;
  border-top: 1px solid #EBEDF5;
  margin-top: 0;
  @media(max-width: 991px){
    flex-direction: column;
    align-items: flex-start;
  }
}
    #textPlace{
      padding: 1.5rem;
      width: calc(100% - 3rem);
      border: none;
      display: block;
      min-height: 300px;
      font-family: $primary-font-family;
      font-size: 1.25rem;
      &:focus{
        outline: 0;
      }
    }
    p {
      margin-bottom: 0;
      padding-bottom: .25rem;
      span {
        display: inline-block;
      color: #596080;
      opacity: .6;
          margin-right: .5rem;
  @media(max-width: 991px){
    margin-bottom: 6px;
  }
        &:last-child{
          margin-right: 0;
        }
      }
      button {
        border: none;
        padding: .5rem 1rem;
        border-radius: 10px;
        font-size: 1rem;
        cursor: pointer;
  @media(max-width: 991px){
    align-self: flex-end;
  }
      }
    }
</style>
