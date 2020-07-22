<template>
  <article class="container">
    <section class="main">
      <b-card no-body class="overflow-hidden">
        <b-row no-gutters>
          <b-col md="6">
            <b-card-img src="images/selfie.png" alt="Image" class="rounded-0"></b-card-img>
          </b-col>
          <b-col md="6">
            <b-card-body title="Horizontal Card">
              <b-card-text>
                This is a wider card with supporting text as a natural lead-in to additional content.
                This content is a little bit longer.
              </b-card-text>
            </b-card-body>
          </b-col>
        </b-row>
      </b-card>
    </section>
  </article>
</template>

<script>
export default {
  head(){
  return{
      title: "Eric's Portfolio About",
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
.container {
  height: 100vh;
}
.main {
  border: 1px solid red;
  margin-top: 10%;
  width: 100%;
}
img {
  max-width: 100%;
}
p {
  margin-left: 10%;
}
</style>