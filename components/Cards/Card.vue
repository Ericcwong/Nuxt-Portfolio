<template>
  <article class="cardPreview">
    <img class="cardThumbnail" v-bind:src="thumbnail" />
    <div class="cardContent">
      <h1>{{title}}</h1>
      <p>{{description}}</p>
    </div>
  </article>
</template>

<script>
export default {
  name: "Card",
  props: {
    id: {
      type: Number,
      required: true
    },
    title: {
      type: String,
      required: true
    },
    description: {
      type: String,
      required: true
    },
    thumbnail: {
      type: String,
      required: true
    }
  }
};
</script>

<style scoped>
.cardPreview {
  border: 1px solid #ccc;
  box-shadow: 0 2px 2px #ccc;
  background-color: white;
  width: 100%;
}
.cardPreview img {
  width: 100%;
}

a {
  text-decoration: none;
  color: black;
}

@media (min-width: 850px) {
  .cardPreview {
    width: 400px;
    margin: 10px;
  }
}

.cardThumbnail {
  width: 100%;
  height: 300px;
  background-position: center;
  background-size: cover;
}

.cardContent {
  padding: 10px;
  text-align: center;
}

/* a:hover .cardPontent,
a:active .cardPontent {
  background-color: #ccc;
} */
</style>