<template>
  <p>Reaction time - {{ score }} ms</p>
  <p class="rank">{{ rank }}</p>
</template>

<script>
export default {
  props: ['score'],
  data() {
    return {
      rank : null
    }
  },
  mounted() {
    if (this.score < 250) {
      this.rank = 'Lightning Fast!'
    } else if (this.score < 400) {
      this.rank = 'Pretty Quick'
    } else {
      this.rank = 'Pokey Pace'
    }
  }
}
</script>

<style>
    .rank {
        font-size: 1.6rem;
        color:rgb(51, 83, 224);
        font-weight: bold;
    }
</style>