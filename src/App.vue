<template>
  <input @keyup="showMessage($event)" />
  <h1>{{ message }}</h1>
  <p v-text="message"></p>

  <div v-html="link"></div>

  <Counter />

  <Counter :counter="initialValue" />

  <Counter counter="2" />

  <Counter counter="3" />

  <Counter counter="-7" />
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
  },
  computed: {
    initialValue() {
      return 7 * 7;
    },
  },

}
</script>
