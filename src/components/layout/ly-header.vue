<template>
<div class="ly-header">
<h1>Case converter</h1>
<p>Standard case convert compilator for your text. Enter your text and choose the case you want to convert it to.</p>
</div>
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
  padding: 3rem 0 7rem;
  text-align: center;
  position: relative;
  background: #fff;
@media(max-width: 991px){
  padding: 2rem 0 8rem;
}
&:before{
  content: '';
  background-image: url(https://media.istockphoto.com/vectors/letters-abstract-background-vector-id1220125097?k=20&m=1220125097&s=612x612&w=0&h=bHUwyy73d_29qrQpZbtkw3KU7nQ00hORNE5v66v9JKM=);
position: absolute;
inset: 0;
opacity: .04;
z-index: 0;
}
  h1 {
    font-size: 3rem;
    letter-spacing: 1px;
  z-index: 1;
  position: relative;
  margin-bottom: 20px;
@media(max-width: 991px){
  margin-top: 0;
  font-size: 2rem;
}
  }
  p {
    font-size: 1.25rem;
    color: #596080;
    font-weight: 300;
    max-width: 700px;
    line-height: 1.5;
    margin: 0 auto; 
@media(max-width: 991px){
  font-size: 1rem;
}
  }
}
</style>
