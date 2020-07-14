<template>
  <div class="contact">
    <h1>Contact Information</h1>
    <div class="container">
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
          <h4>Email: Ericwong12@live.com</h4>
        </div>
        <div class="phoneNumber">
          <a href="tel:+18019318459">
            <div class="icon">
              <font-awesome-icon :icon="['fas', 'mobile-alt']" />
            </div>
          </a>
          <h4>Phone: 801-931-8459</h4>
        </div>
        <div class="socialMedia">
          <a href="tel:+18019318459">
            <div class="icon">
              <font-awesome-icon :icon="['fab', 'linkedin']" />
            </div>
          </a>
          <h4>LinkedIn</h4>
        </div>
        <div class="socialMedia">
          <a href="https://github.com/Ericcwong">
            <div class="icon">
              <font-awesome-icon :icon="['fab', 'github']" />
            </div>
          </a>
          <h4>Github</h4>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "contact"
};
</script>

<style scoped>
.contact {
  margin: 0 auto;
  justify-content: center;
  align-items: center;
  text-align: center;
}
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  /* flex-direction: column; */
  flex-grow: 2;
  flex-wrap: wrap;
  justify-content: center;
  justify-content: space-evenly;
  align-items: center;
  text-align: center;
  /* border: 1px black solid; */
}
p {
  font-size: 1.25rem;
}
.container > div {
  flex: 0 50%;
}
.icon {
  font-size: 5rem;
}
a {
  color: inherit;
}
a:hover {
  color: lightblue;
}
@media only screen and (max-width: 775px) {
  .container {
    flex-direction: column;
  }
}
</style>
