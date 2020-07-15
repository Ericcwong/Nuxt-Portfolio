<template>
  <div class="NavBar">
    <b-navbar toggleable="lg" type="light" variant>
      <b-navbar-brand>
        <nuxt-link to="/" class="title">
          <h1>Eric Wong</h1>
          <h2>Portfolio</h2>
        </nuxt-link>
      </b-navbar-brand>

      <b-navbar-toggle target="nav-collapse">
        <template v-slot:default="{ expanded }">
          <font-awesome-icon v-if="expanded" :icon="['fas', 'chevron-up']" />
          <font-awesome-icon v-else :icon="['fas', 'chevron-down']" />
          <!-- <b-icon v-if="expanded" font-awesome-icon :icon="['fas', 'envelope']"></b-icon> -->
          <!-- <b-icon v-else font-awesome-icon :icon="['fas', 'envelope']"></b-icon> -->
        </template>
      </b-navbar-toggle>

      <b-collapse id="nav-collapse" is-nav>
        <!-- Right aligned nav items -->
        <b-navbar-nav class="ml-auto">
          <ContactSideBar />
          <nuxt-link to="/">
            <b-button class="navLink my-2 my-sm-0 ml-2" variant="outline-secondary">Home</b-button>
          </nuxt-link>
          <nuxt-link to="projects">
            <b-button class="navLink my-2 my-sm-0 ml-2" variant="outline-secondary">Projects</b-button>
          </nuxt-link>
          <nuxt-link to="resume">
            <b-button class="navLink my-2 my-sm-0 ml-2" variant="outline-secondary">Resume</b-button>
          </nuxt-link>
          <nuxt-link to="about">
            <b-button class="navLink my-2 my-sm-0 ml-2" variant="outline-secondary">About</b-button>
          </nuxt-link>
          <b-button
            class="navLink my-2 my-sm-0 ml-2"
            variant="outline-secondary"
            v-b-toggle.directive-variant
          >Contact</b-button>
        </b-navbar-nav>
      </b-collapse>
    </b-navbar>
  </div>
</template>

<script>
import ContactSideBar from "./ContactSideBar";
export default {
  name: "NavBar",
  components: {
    ContactSideBar
  }
};
</script>

<style scoped>
.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  font-weight: 300;
  font-size: calc(30px + (50 - 30) * ((100vw - 300px) / (1600 - 300)));
  /* color: #6c757d; */
  color: black;
  text-align: center;
}

.NavBar {
  background: white;
  border-bottom: 4px solid lightgray;
}
</style>