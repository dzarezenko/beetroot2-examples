<template>
  <input @keyup="showMessage($event)" />
  <h1>{{ message }}</h1>
  <p v-text="message"></p>

  <div v-html="link"></div>
</template>

<script>
export default {
  data() {
    return {
      message: "Hello World!!!",
      link: `<a href="http://www.google.com">Google</a>`,
    }
  },
  methods: {
    showMessage(event) {
      this.message = event.target.value;
    }
  }
}
</script>
