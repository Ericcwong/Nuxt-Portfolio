<template>
  <article>
    <b-carousel
      class="carousel"
      id="carousel-fade"
      style="text-shadow: 0px 0px 2px #000"
      fade
      indicators
    >
      <b-carousel-slide caption="First slide" img-src="https://picsum.photos/1024/480/?image=10"></b-carousel-slide>
      <b-carousel-slide caption="Second Slide" img-src="https://picsum.photos/1024/480/?image=12"></b-carousel-slide>
      <b-carousel-slide caption="Third Slide" img-src="https://picsum.photos/1024/480/?image=22"></b-carousel-slide>
    </b-carousel>
  </article>
</template>

<script>
export default {};
</script>

<style scoped>
article {
  min-height: 100vh;
}
.carousel {
  height: 100px !important;
}
</style>