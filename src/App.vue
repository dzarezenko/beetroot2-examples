<template>
  <input @keyup="showMessage($event)" />
  <h1>{{ message }}</h1>
  <p v-text="message"></p>

  <div v-html="link"></div>

  <Counter />

  <Counter />

  <Counter />

  <Counter />

  <Counter />
</template>

<script>
import Counter from "./components/Counter";

export default {
  components: {
    Counter
  },
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
