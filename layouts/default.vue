<template>
  <article>
    <NavBar />
    <nuxt />
    <Footer />
  </article>
</template>
<script>
import NavBar from "../components/NavBar/NavBar";
import Footer from "../components/Footer";
export default {
  components: {
    NavBar,
    Footer
  }
};
</script>
<style scoped>
#background {
  background: #c0c0c0;
}
</style>
