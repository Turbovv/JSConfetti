<template>
  <h1 @click="showConfetti">🎉 Press me! {{counter}}</h1>
</template>

<script>
import JSConfetti from 'js-confetti'

const confetti = new JSConfetti()

export default {
  data() {
    return {
      counter:-1
    }
  },
  mounted() { 
    this.showConfetti()
  },
  methods: {
    showConfetti() {
      confetti.addConfetti()
      this.counter++
    }
  },
}
</script>

<style>
h1 {
  text-align: center;
  cursor: pointer;
  margin-top: 3em;
}
</style>