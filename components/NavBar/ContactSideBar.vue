<template>
  <div>
    <b-sidebar id="directive-variant" bg-variant="light" text-variant="dark" shadow>
      <div class="px-3 py-2">
        <div class="contact">
          <h1>Contact Information</h1>

          <div class="contactText">
            <p>To get in touch, you can reach me with anyone of these links.</p>
          </div>
          <div class="contactInfo">
            <div class="email">
              <a href="mailto:ericwong12@live.com">
                <div class="icon">
                  <font-awesome-icon :icon="['fas', 'envelope']" />
                </div>
              </a>
              <p>Email: Ericwong12@live.com</p>
            </div>
            <div class="phoneNumber">
              <a href="tel:+18019318459">
                <div class="icon">
                  <font-awesome-icon :icon="['fas', 'mobile-alt']" />
                </div>
              </a>
              <p>Phone: 801-931-8459</p>
            </div>
            <div class="socialMedia">
              <a href="https://www.linkedin.com/in/eric-wong-b721bbb2/" target="_blank">
                <div class="icon">
                  <font-awesome-icon :icon="['fab', 'linkedin']" />
                </div>
              </a>
              <p>LinkedIn</p>
            </div>
            <div class="socialMedia">
              <a href="https://github.com/Ericcwong" target="_blank">
                <div class="icon">
                  <font-awesome-icon :icon="['fab', 'github']" />
                </div>
              </a>
              <p>Github</p>
            </div>
          </div>
          <ContactSideBarForm />
        </div>
      </div>
    </b-sidebar>
  </div>
</template>

<script>
import ContactSideBarForm from "./ContactSideBarForm";
export default {
  name: "ContactSideBar",
  components: {
    ContactSideBarForm
  }
};
</script>

<style scoped>
.icon {
  font-size: calc(14px + (50 - 14) * ((100vw - 300px) / (1600 - 300)));
}
a {
  color: inherit;
}
a:hover {
  color: lightblue;
}
button {
  /* margin-left: 5px;
  margin-right: 5px; */
  /* display: inline-block; */
}
@media only screen and (max-width: 775px) {
  .icon {
    font-size: 2.5rem;
  }
}
</style>
