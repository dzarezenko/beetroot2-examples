<template>
  <input @keyup="showMessage($event)" />
  <h1>{{ message }}</h1>
  <p v-text="message"></p>

  <div v-html="link"></div>

  <Counter color="cl-red" />

  <Counter color="cl-green" :counter="initialValue" />

  <Counter color="cl-blue" counter="2" />

  <Counter color="cl-orange" counter="3" />

  <Counter color="cl-purple" counter="-7" />
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
