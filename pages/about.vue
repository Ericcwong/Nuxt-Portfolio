<template>
  <article class="container">
    <section class="main">
      <b-card no-body class="overflow-hidden">
        <b-row no-gutters>
          <b-col md="5">
            <b-card-img src="images/selfie.png" alt="Image" class="rounded-0"></b-card-img>
          </b-col>
          <b-col md="7">
            <b-card-body>
              <b-card-title class="title" title="I like to build, break, and fix things"></b-card-title>
              <b-card-text>
                Hello, Eric here! I am currently living in West Jordan, Utah. I recently graduated from University of Utah's full stack web developer bootcamp. I work with Nuxtjs as a front end framework mostly and am familiar with Vue and as well as React.
                Back end databases I worked with MongoDB and Firebase.
                I am currently open for any web developer position
              </b-card-text>
              <b-card-title class="title" title="Current focus"></b-card-title>
              <b-card-text>My focus after the bootcamp is to continue to learn on my own and challenge myself to refine past projects. Along side refining is to find experience in the web development field and entry level position or internship.</b-card-text>
              <b-card-title class="title" title="Languages and Tech"></b-card-title>
              <b-card-text>
                <LanguageIcons />
              </b-card-text>
            </b-card-body>
          </b-col>
        </b-row>
      </b-card>
      <br />
      <b-card no-body class="overflow-hidden">
        <b-row no-gutters>
          <b-col md="6">
            <b-card-img src="images/keyboard.webp" alt="Image" class="rounded-0"></b-card-img>
          </b-col>
          <b-col md="6">
            <b-card-body>
              <b-card-title class="title" title="Custom keyboard"></b-card-title>
              <b-card-text>
                A keyboard is something I use on a daily basis and I never thought much of it, that is until I watch a few videos about custom mechanical keyboards. After watching a couple it started to spiral out of control. I started to research on
                everything that a mechanical keyboard needed reading subreddits and countless videos on how to build one. The videos did not do justifcation on how hard
                and time consuming keyboard building is if you choose to go with the soldering route. After I was done building the keyboard I was so happy that it was over and two months later I still cannot stop typing on it. Although the build being over I do have to say I do miss the building hobby and I would want
                to build another one in the near future.
              </b-card-text>
            </b-card-body>
          </b-col>
        </b-row>
      </b-card>
    </section>
  </article>
</template>

<script>
import LanguageIcons from '~/components/About/LanguageIcons'
export default {
  components: {
    LanguageIcons,
  },
  head() {
    return {
      title: "Eric's Portfolio About",
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
.container {
  min-height: 100vh;
}
.main {
  margin-top: 10%;
  width: 100%;
}
img {
  /* max-width: 100%; */
}
.title {
  border-bottom: 1px solid darkgray;
}
.col-md-6 {
  margin-top: 10px;
}
</style>