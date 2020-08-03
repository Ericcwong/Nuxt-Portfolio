<template>
  <article>
    <section>
      <div class="heading">
        <h1>that I have developed during my bootcamp and independently</h1>
      </div>
    </section>
    <section class="cards">
      <CardData />
    </section>
  </article>
</template>

<script>
import CardData from '~/components/PortfolioCards/PortfolioCardList'

export default {
  components: {
    CardData,
  },
  //Handles Browsers tab information and search
  head() {
    return {
      title: "Eric's Portfolio Projects",
      meta: [
        { name: 'Project', content: 'Web developer portfolio projects' },
        { name: 'keywords', content: 'Nuxt, Web developer, Hire me' },
        { name: 'author', content: 'Eric Wong' },
      ],
    }
  },
  methods: {},
}
</script>

<style scoped>
.heading {
  font-size: 40px;
  text-align: center;
  color: black;
  background-color: lightgray;
}
.cards {
  display: flex;
}
</style>