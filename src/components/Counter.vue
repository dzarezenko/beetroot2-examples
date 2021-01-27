<template>
  <div>

    <h1 :style="`color: ${color}`">{{ counter }}</h1>
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
  /*data() {
    return {
      counter: 0,
    }
  }*/
}
</script>

<style scoped>
h1 {
  color: blue;
  display: inline;
}
</style>
