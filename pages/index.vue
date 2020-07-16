<template>
  <div>
    <div class="home">
      <div class="title">
        <h1 data-aos="fade-down" data-aos-duration="3000">Eric Wong</h1>
        <h3 class="subtitle" data-aos="fade-up" data-aos-duration="3000">Full Stack Web developer</h3>

        <div class="links">
          <nuxt-link to="projects">
            <h4 data-aos="fade-right" data-aos-duration="3000">Projects</h4>
          </nuxt-link>
          <a href="https://www.linkedin.com/in/eric-wong-b721bbb2/" target="_blank">
            <h4 data-aos="fade-left" data-aos-duration="3000">LinkedIn</h4>
          </a>
        </div>
      </div>
    </div>
    <HomeInfo />
  </div>
</template>

<script>
import HomeInfo from "~/pages/home/HomeInfo"

export default {
  components: {
    HomeInfo
  },
head(){
  return{
      title: "Eric's Portfolio Home",
      meta:[
        {name: "Home", content: "Web developer portfolio"},
        {name: "keywords", content: "Nuxt, Web developer, Hire me"},
        {name: "author", content: "Eric Wong"}
      ]
  }

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
  flex-direction: column;
  background: url('~assets/images/homeBackground.jpg') no-repeat center;
  -webkit-background-size: cover;
  /* background-position: bottom right; */
  /* -moz-background-size: cover; */
  /* -o-background-size: cover; */
  /* background-size: cover; */
}
.title,
h1,
h2 {
  font-size: 5rem;
  color: white;
}
.links {
  display: flex;
  justify-content: center;
  flex-direction: row;
  justify-content: space-evenly;
}
h4 {
  color: white;
  border: 1px solid white;
}
a {
  text-decoration-color: black;
}
</style>
