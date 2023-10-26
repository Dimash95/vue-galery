<template>
  <div class="main-container">
    <Header />
    <div class="main-content">
      <router-view />
    </div>
    <Footer />
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Footer from "./components/Footer.vue";

export default {
  components: { Header, Footer },
};
</script>

<style>
@import "./style.css";

.main-content {
  min-height: calc(100vh - 200px);
}
</style>
