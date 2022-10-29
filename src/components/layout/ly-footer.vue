<template>
  <footer class="ly-footer">
    <div class="container">
      <p>
        © <span id="year" class="d-inline-block">2022</span> | Made with 💜 by
        <a href="https://davidkolisek.netlify.app/" target="_blank"
          >davidkolisek</a
        >
      </p>
    </div>
  </footer>
</template>

<script>
export default {
//   mounted: function () {
//   this.$nextTick(function () {
//     getYear() {
//       document.getElementById("year").innerHTML = new Date().getFullYear();
//     }
//   })
// }
};
</script>

<style lang="scss" scoped>
footer {
  background: $c-secondary-900;
  text-align: center;
  padding: 1rem 0;
  p {
    margin: 0;
    padding: 0.5rem 0;
    font-weight: 500;
    font-size: 0.8rem;
    color: #596080;
    a {
      color: #fff;
      text-decoration: underline;
    }
  }
}
</style>
