<template>
  <input v-model="message" />
  <h1>{{ msg }}</h1>
</template>

<script>
export default {
  data() {
    return {
      msg: "Hello World!!!",
    }
  },
  computed: {
    message: {
      set: function(val) {
        // ....

        this.msg = val;
      },
      get: function() {
        // ...

        return this.msg;
      }
    }
  }
}
</script>
