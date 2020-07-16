<template>
  <b-container fluid>
    <div class="footer">
      <div class="footer-content">
        <b-row>
          <b-col>
            <h5>Stay Connected</h5>
            <div class="icons">
              <a
                href="https://www.linkedin.com/in/eric-wong-b721bbb2/"
                target="_blank"
                v-b-tooltip.hover
                title="LinkedIn"
              >
                <font-awesome-icon :icon="['fab', 'linkedin']" />
              </a>
              <a
                href="https://github.com/ericcwong"
                target="_blank"
                v-b-tooltip.hover
                title="Github"
              >
                <font-awesome-icon :icon="['fab', 'github']" />
              </a>
            </div>
          </b-col>
          <b-col>
            <h5>Quick Links</h5>
            <ul>
              <li class="icons">
                <nuxt-link to="/" v-b-tooltip.hover title="Home">
                  <font-awesome-icon :icon="['fas', 'home']" />
                </nuxt-link>
              </li>
              <li class="icons">
                <nuxt-link to="/projects" v-b-tooltip.hover title="PortFolio">
                  <font-awesome-icon :icon="['fas', 'briefcase']" />
                </nuxt-link>
              </li>
              <li class="icons">
                <nuxt-link to="/resume" v-b-tooltip.hover title="Resume">
                  <!-- Reason its so long is because fontawesome didnt have the icon but bootstrap did -->
                  <font-awesome-icon :icon="['fas', 'file-pdf']" />
                </nuxt-link>
              </li>
              <li class="icons">
                <nuxt-link to="/about" v-b-tooltip.hover title="About Me">
                  <font-awesome-icon :icon="['fas', 'address-card']" />
                </nuxt-link>
              </li>
              <li class="icons">
                <a v-b-tooltip.hover title="Contact" v-b-toggle.directive-variant>
                  <font-awesome-icon :icon="['fas', 'comment-dots']" />
                </a>
              </li>
            </ul>
          </b-col>
        </b-row>
      </div>
      <!-- Bottom of the footer -->
      <div class="footer-bottom">
        <client-only>
          <p>
            <font-awesome-icon :icon="['far', 'copyright']" />Eric Wong
            <!-- Updates to current year -->
            <span>{{new Date().getFullYear()}}</span>
          </p>
        </client-only>
      </div>
    </div>
  </b-container>
</template>

<script>
import ContactSideBar from "../components/NavBar/ContactSideBar";
export default {
  name: "Footer",
  components: {
    ContactSideBar
  },
  head() {
    return {
      script: [{ src: "https://unpkg.com/@popperjs/core@2/dist/umd/popper.js" }]
    };
  }
};
</script>

<style scoped>
.container {
  height: 100%;
}
.footer {
  position: relative;
  height: 100%;
  background: #c0c0c0;
}
.footer .footer-bottom {
  bottom: 0;
  left: 0;
  text-align: center;
  position: relative;
  width: 100%;
  padding-top: 20px;
  background: lightgray;
}
.nav-link {
  color: inherit;
  font-size: 1.25rem;
}
.nav-link:hover {
  color: lightgray;
}
.col {
  text-align: center;
}
.icons {
  font-size: 3rem;
}
ul > li {
  display: inline-block;
  /* You can also add some margins here to make it look prettier */
  zoom: 1;
  *display: inline;
  margin-left: 5px;
  margin-right: 5px;
  /* this fix is needed for IE7- */
}
a {
  color: inherit;
}
</style>