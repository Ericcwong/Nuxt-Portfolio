<template>
  <article>
    <section>
      <div class="heading">Projects that I have developed during my bootcamp and on my own.</div>
    </section>
    <section class="cards">
      <CardData />
    </section>
  </article>
</template>

<script>
import CardData from './ProjectCards/'

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
  font-size: 18px;
  text-align: center;
}
.cards {
  display: flex;
}
</style>