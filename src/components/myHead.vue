<template>
  <div class="text-xs-center">
    <v-progress-circular :width="7" color="primary" :size="70" :value="currentQuote*10">{{ currentQuote }}/10</v-progress-circular>
  </div>
</template>

<script>
export default {
  name: "myHead",
  props: ["currentQuote"]
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
