<template>
  <!-- <article class="cardPreview">
    <img class="cardThumbnail" v-bind:src="thumbnail" />
    <div class="cardContent">
      <h1>{{title}}</h1>
      <p>{{description}}</p>
    </div>
  </article>-->
  <div>
    <b-card no-body class="cardPreview overflow-hidden">
      <b-row no-gutters>
        <b-col md="6">
          <b-card-img v-bind:src="thumbnail" alt="Image" class="rounded-0"></b-card-img>
        </b-col>
        <b-col md="6">
          <b-card-body :title="title">
            <b-card-text>{{description}}</b-card-text>
          </b-card-body>
        </b-col>
      </b-row>
      <template v-slot:footer>
        <a :href="link" role="button">Link</a>
      </template>
    </b-card>
  </div>
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
    },
    link:{
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
  max-width: 100%;
  height: 449px;
}

a {
  text-decoration: none;
  color: black;
}

@media (min-width: 850px) {
  .cardPreview {
    width: 900px;
    height: auto;
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
</style>