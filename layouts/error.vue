<template>
  <div class="container">
    <h1 v-if="error.statusCode === 404">Sorry, Page was not found.</h1>
    <img src="images/Dog Swimming/Dog-swimming-01.svg" alt="Dog in floaty" />
    <button class="btn btn-primary">
      <nuxt-link to="/">Back to Home</nuxt-link>
    </button>
  </div>
</template>

<script>
export default {
  props: ['error'],
}
</script>

<style scoped>
h1 {
  text-align: center;
}
a {
  color: white;
}
img {
  width: 75%;
  margin: 0 auto;
}
</style>