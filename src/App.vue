<template>
  <div>
    <Navbar></Navbar>
    <Content>
      <router-view></router-view>
    </Content>
    <Footer/>
  </div>
</template>
<script>
import Navbar from "./components/layout/ly-navigation";
import Footer from "./components/layout/ly-footer";
import Content from "./components/layout/ly-content";
export default {
  components: {
    Navbar,
    Footer,
    Content,
  }
};
</script>