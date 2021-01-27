<template>
  <input @keyup="showMessage($event)" />
  <h1>{{ message }}</h1>
</template>

<script>
export default {
  data() {
    return {
      message: "Hello World!!!",
    }
  },
  methods: {
    showMessage(event) {
      this.message = event.target.value;
    }
  },
}
</script>
