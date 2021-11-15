<template>
    <!-- <Navbar></Navbar> -->
    <Header></Header>
    <Content>
      <router-view></router-view>
    </Content>
    <Footer/>
</template>
<script>
import Header from "./components/layout/ly-header";
// import Navbar from "./components/layout/ly-navigation";
import Footer from "./components/layout/ly-footer";
import Content from "./components/layout/ly-content";
export default {
  components: {
    // Navbar,
    Footer,
    Content,
    Header
  }
};
</script>