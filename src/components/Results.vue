<template>
  <h2>Results</h2>
  <p>{{ score }} ms</p>
  <h3> {{ rank }}</h3>
</template>

<script>
  export default {
    props: ["score",],
    data() {
      return {
        rank: null,
      }
    },
    mounted() {
      if (this.score < 200) {
        this.rank = "Sheeeesh"
      } else if (this.score < 350) {
        this.rank = "Not tooo bad"
      } else {
        this.rank = "Slow Ass"
      }
    }
  }
</script>

<style>
  .rank {
    font-size: 1.4em;
    color: #0faf87;
    font-weight: bold;
  }
</style>