<template>
  <div>
    <h4>Message me here!</h4>
    <form method="POST" @submit="checkForm">
      <label>Name</label>
      <input type="text" name="name" />
      <!-- <label>Email</label>
      <input type="email" name="email" />
      <label>Message</label>
      <textarea name="message"></textarea>-->
      <input type="submit" value="submit" />
    </form>
  </div>
</template>

<script>
export default {
  name: "ContactSideBarForm",
  data() {
    return {
      name: null
      //   email: null,
      //   message: null
    };
  },
  methods: {
    checkForm: function(e) {
      if (this.name) {
        return true;
      }

      this.errors = [];

      if (!this.name) {
        this.errors.push("Name required.");
      }

      e.preventDefault();
    }
  }
};
</script>

<style scoped>
input {
  border: black;
}
</style>