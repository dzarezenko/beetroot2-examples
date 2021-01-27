<template>
  <div>

    <h1>{{ counter }}</h1>
    <button @click="counter--">-</button><button @click="counter++">+</button>

  </div>  
</template>

<script>
export default {
  data() {
    return {
      counter: 0,
    }
  }
}
</script>

<style scoped>
h1 {
  color: blue;
  display: inline;
}
</style>
