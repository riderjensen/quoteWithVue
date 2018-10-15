<template>
  <div id="app">
		<v-app>
			<v-layout row>
			<v-flex xs12 sm3 > </v-flex>
			<v-flex xs12 sm6 >
				<myHead :currentQuote="quoteArray.length" />
				<myInput v-on:newQuote="addQuote"/>
				<quoteContainer :quoteArray="quoteArray"/>
			</v-flex>
			<v-flex xs12 sm3 > </v-flex>
			</v-layout>
	   	</v-app>
  </div>
</template>

<script>
import myHead from "./components/myHead.vue";
import myInput from "./components/myInput.vue";
import quoteContainer from "./components/quoteContainer";

export default {
  name: "app",
  components: {
    myHead,
    myInput,
    quoteContainer
  },
  data: () => {
    return {
      quoteArray: []
    };
  },
  methods: {
    addQuote(quote) {
      if (this.quoteArray.length >= 10) {
        alert("Please delete a quote first");
      } else {
        this.quoteArray.push(quote);
      }
    }
  }
};
</script>

<style>
#app {
  color: #2c3e50;
}
</style>
