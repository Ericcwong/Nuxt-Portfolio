<template>
  <article>
    <section>
      <b-form-group label="Project filter">
        <b-form-radio-group v-model="selected" :options="options" name="radio-inline"></b-form-radio-group>
      </b-form-group>

      <div class="mt-3">
        Selected:
        <strong>{{ selected }}</strong>
      </div>
    </section>
    <section>
      <div v-show="selected === 'All'"></div>
      <div v-show="selected === 'React'">
        <ReactData />
      </div>
    </section>
  </article>
</template>

<script>
import ReactData from "./ProjectCards/React"
export default {
  components:{
    ReactData
  },
 //Data for radio buttons
 data() {
      return {
        selected: 'Favorite',
        options: [
          { text: "Favorite Projects", value: 'Favorite' },
          { text: 'Nuxt Fullstack', value: 'Nuxt' },
          { text: 'React Fullstack', value: 'React' },
          { text: 'Vanilla Fullstack', value: 'Vanilla' },
          { text: "All Projects", value: 'All' }
        ]
      }
    },
  //Handles Browsers tab information and search
  head(){
  return{
      title: "Eric's Portfolio Projects",
      meta:[
        {name: "Project", content: "Web developer portfolio projects"},
        {name: "keywords", content: "Nuxt, Web developer, Hire me"},
        {name: "author", content: "Eric Wong"}
      ]
  }

}
};
</script>

<style scoped>
</style>