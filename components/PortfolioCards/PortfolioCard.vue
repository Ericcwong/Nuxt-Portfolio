<!-- Structures portfolio cards-->
<template>
  <div class="card" data-aos-duration="2000" v-bind:data-aos="classes">
    <b-card no-body class="cardPreview overflow-hidden h-100">
      <b-row no-gutters>
        <b-col md="7">
          <b-card-img
            v-bind:src="thumbnail"
            :srcset="`${thumbnail} 1x, ${thumbnail} 2x`"
            alt="Image"
            class="rounded-0"
          ></b-card-img>
        </b-col>
        <b-col md="5">
          <b-card-body>
            <b-card-title>{{title}}</b-card-title>
            <b-card-sub-title>Framework: {{framework}}</b-card-sub-title>
            <br />
            <b-card-text>
              {{description}}
              <br />
              {{subDescription}}
            </b-card-text>
          </b-card-body>
        </b-col>
      </b-row>
      <template v-slot:footer>
        <a :href="deployLink" role="button">
          <font-awesome-icon :icon="['fas','location-arrow']" />Deploy Link
        </a>
        <a :href="githubLink" role="button">
          <font-awesome-icon :icon="['fab','github']" />GitHub Link
        </a>
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
    classes: {
      type: String,
    },
    title: {
      type: String,
      required: true,
    },
    description: {
      type: String,
      required: true,
    },
    subDescription: {
      type: String,
    },
    thumbnail: {
      type: String,
      required: true,
    },
    deployLink: {
      type: String,
    },
    githubLink: {
      type: String,
    },
    framework: {
      type: String,
    },
  },
}
</script>

<style scoped>
.card {
  border: none;
}
.cardPreview {
  border: 1px solid lightgray;
  box-shadow: 0 2px 2px #ccc;
  background-color: white;
  width: 100%;
}

.card-subtitle {
  border-bottom: 1px solid darkgray;
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