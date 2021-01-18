<template>
  <p>Reaction Time - {{ score }} ms</p>
  <p class="rank">{{ rank }}</p>
</template>

<script>
export default {
  props: ['score'],
  data() {
    return {
      rank: null,
    };
  },
  mounted() {
    if (this.score < 250) {
      this.rank = 'Blazing Fast';
    } else if (this.score < 400) {
      this.rank = 'Decently Fast';
    } else {
      this.rank = 'Are you fit for duty?';
    }
  },
};
</script>

<style scoped>
.rank {
  font-size: 1.4rem;
  color: crimson;
  font-weight: bold;
}
</style>
