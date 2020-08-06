<!--Structures the Home Cards -->
<template>
  <div>
    <b-card no-body class="cardPreview overflow-hidden">
      <b-row no-gutters>
        <b-col md="4">
          <b-card-img v-bind:src="thumbnail" alt="Image" class="rounded-0"></b-card-img>
        </b-col>
        <b-col md="7">
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
  name: 'Card',
  props: {
    id: {
      type: Number,
      required: true,
    },
    title: {
      type: String,
      required: true,
    },
    description: {
      type: String,
      required: true,
    },
    thumbnail: {
      type: String,
      required: true,
    },
    link: {
      type: String,
    },
    gitlink: {
      type: String,
    },
  },
}
</script>

<style scoped>
.cardPreview {
  box-shadow: 0 2px 2px #ccc;
  background-color: white;
}
.cardPreview img {
  height: 275px;
}

a {
  text-decoration: none;
  color: black;
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
@media (min-width: 850px) {
  .cardPreview {
    width: 900px;
    height: auto;
    margin: 10px;
  }
}
@media (max-width: 768px) {
  .cardPreview img {
    height: 100%;
  }
}
</style>