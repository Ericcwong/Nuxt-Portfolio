<template>
  <div>
    <div class="home">
      <div class="title">
        <h1>Eric Wong</h1>
        <h2 class="subtitle">Full Stack Web developer</h2>
        <!-- <div class="links">
            <a href="https://nuxtjs.org/" target="_blank" class="button--green">Documentation</a>
            <a href="https://github.com/Ericcwong" target="_blank" class="button--grey">GitHub</a>
        </div>-->
      </div>
    </div>
    <HomeInfo />
  </div>
</template>

<script>
import Logo from "../components/Logo";
import HomeInfo from "./home/HomeInfo";

export default {
  components: {
    Logo,
    HomeInfo
  }
};
</script>

<style scoped>
.home {
  margin: 0 auto;
  min-height: 90vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
  background: url('~assets/images/homeBackground.jpg') no-repeat center;
  -webkit-background-size: cover;
  /* -moz-background-size: cover; */
  /* -o-background-size: cover; */
  /* background-size: cover; */
}
.title {
  background-color: white;
  width: 100%;
}
</style>
