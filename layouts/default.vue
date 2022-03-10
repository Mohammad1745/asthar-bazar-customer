<template>
  <div class="wrapper">
    <div class="sidebar">
      <sidebar />
    </div>
    <div class="content">
      <div class="header">
        <navbar />
      </div>
      <div class="main">
        <Nuxt />
      </div>
      <div class="footer">
        <Footer />
      </div>
    </div>
  </div>
</template>

<script>
  import Sidebar from "../components/default/Sidebar";
  import Navbar from "../components/default/header/Navbar";
  import Footer from "../components/default/Footer";
  export  default {
    components: {Sidebar, Navbar, Footer}
  }
</script>

<style scoped>
@import '~/assets/css/layouts.css';
@import '~/assets/css/layouts-responsive.css';
</style>
