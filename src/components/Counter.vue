<template>
  <div>

    <h1 :class="[color, cls]" class="italic">{{ counter }}</h1>
    <button @click="counter--">-</button><button @click="counter++">+</button>

  </div>  
</template>

<script>
export default {
  props: {
    counter: {
      type: Number,
      default: 0
    },
    color: String,
  },
  data() {
    return {
      cls: 'bold'
    }
  }
}
</script>

<style scoped>
h1 {
  display: inline;
}

h1.italic {
  font-style: italic;
}

h1.bold {
  font-weight: bold;
}

h1.cl-red {
  color: red;
}
h1.cl-green {
  color: green;
}
h1.cl-blue {
  color: blue;
}
h1.cl-orange {
  color: orange;
}
h1.cl-purple {
  color: purple;
}
</style>
