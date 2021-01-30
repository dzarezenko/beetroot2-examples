<template>
  <input @keyup="showMessage($event)" />
  <h1>{{ message }}</h1>
  <p v-text="message"></p>

  <div v-html="link"></div>

  <Counter v-for="i in colors.length" :key="i" :color="`cl-${colors[i-1]}`" :counter="counters[i-1]" />

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

      colors: ["red", "green", "blue", "orange", "purple"],
      counters: [7, 13, 21, 9, 3]
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
