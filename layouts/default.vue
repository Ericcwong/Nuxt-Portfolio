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
/* section {
  min-height: 100vh;
  width: 100%;
  background: #ffffff;
} */
/* #test {
  min-height: 100vh;
  margin-bottom: -330px;
  position: relative;
} */
#background {
  background: #c0c0c0;
}
</style>
