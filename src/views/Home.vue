<template>
  <div class="container">
    <div class="text-window">
      <Textplace />
      <ConvertButtons />
      <div class="copied-popup">Copied to your clipboard!</div>
    </div>
  </div>
</template>

<script>
import Textplace from "./modules/Home/TextPlace";
import ConvertButtons from "./modules/Home/ConvertButtons";
export default {
  name: "Home",
  components: { Textplace, ConvertButtons },
  data() {
    return {};
  },
};
</script>

<style lang="scss" scoped>
.text-window {
  display: flex;
  flex-direction: column;
  padding: 2rem 0;
  position: relative;
  z-index: 2;
  margin-top: -90px;
  @media (max-width:991px) {
    flex-direction: column;
    padding: 0 15px 2rem;

  }
}
.copied-popup {
  position: fixed;
  padding: 0.5rem;
  border-radius: 5px;
  color: #fff;
  bottom: -40px;
  opacity: 0;
  left: calc(50% - 110px);
  text-align: center;
  margin: 0 auto;
  width: 220px;
  background: #50cd55;
  transition: all ease 200ms;
  box-shadow: rgba(0, 0, 0, 0.2) 0px 12px 28px 0px,
    rgba(0, 0, 0, 0.1) 0px 2px 4px 0px,
    rgba(255, 255, 255, 0.05) 0px 0px 0px 1px inset;
  &.active {
    transition: all ease 200ms;
    bottom: 3rem;
    opacity: 1;
  }
}
</style>
