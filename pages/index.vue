<template>
  <div>
    <div class="home">
      <div class="title">
        <h1 data-aos="fade-down" data-aos-duration="3000">Eric Wong</h1>
        <h3 class="subtitle" data-aos="fade-up" data-aos-duration="3000">Full Stack Web developer</h3>

        <div class="links">
          <nuxt-link to="projects">
            <h4 data-aos="fade-up" data-aos-duration="3000">Projects</h4>
          </nuxt-link>
          <a rel="noopener" href="https://www.linkedin.com/in/eric-wong-b721bbb2/" target="_blank">
            <h4 data-aos="fade-up" data-aos-duration="3000">LinkedIn</h4>
          </a>
          <a rel="noopener" href="https://github.com/Ericcwong" target="_blank">
            <h4 data-aos="fade-up" data-aos-duration="3000">Github</h4>
          </a>
        </div>
      </div>
    </div>
    <div class="badges">
      <h1 class="badgesTitle">Accomplishments:</h1>
    <HomeCard />
    </div>
    <hr/>
    <div class="projects">
      <h1 class="projectTitle">Projects:</h1>
      <CardData/>
    </div>
  </div>
</template>

<script>
import HomeCard from '~/components/HomeCards/HomeCardList'
import CardData from '~/components/PortfolioCards/PortfolioCardList'

export default {
  components: {
    HomeCard,
    CardData
  },
  head() {
    return {
      title: "Eric's Portfolio Home",
      meta: [
        { name: 'Home', content: 'Web developer portfolio' },
        { name: 'keywords', content: 'Nuxt, Web developer, Hire me' },
        { name: 'author', content: 'Eric Wong' },
      ],
    }
  },
}
</script>

<style scoped>
.home {
  background: url('/images/homeBackground.JPG') no-repeat center;
  margin: 0 auto;
  min-height: 90vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
  flex-wrap: wrap;
  /* flex-direction: column; */
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
.badges{
  display: flex;
  justify-content: space-between;
  flex-wrap: wrap;
}
.badgesTitle, .projectTitle{
  flex: 0 0 100%;
  color: black;
  font-size: 2rem;
  text-align: center;
}
</style>
