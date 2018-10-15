<template>
	<div>
		<quoteCard v-on:delQuote="deleteQuote" v-for="(quote, i) in quoteArray" :key="i" :numInArray="i">{{ quoteArray[i] }}</quoteCard>
	</div>
</template>

<script>
import quoteCard from "./quoteCard.vue";

export default {
  name: "quoteContainer",
  components: {
    quoteCard
  },
  props: ["quoteArray"],
  methods: {
    deleteQuote(index) {
      this.quoteArray.splice(index, 1);
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
