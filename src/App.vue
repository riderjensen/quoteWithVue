<template>
  <div id="app">
		<v-app>
			<v-layout row>

			<v-flex xs12 sm6 offset-sm3>
				<myHead :currentQuote="quoteArray.length" />
				<myInput v-on:newQuote="addQuote"/>
				<quoteContainer :quoteArray="quoteArray"/>
			</v-flex>
			</v-layout>
			<myFooter/>
	   	</v-app>
  </div>
</template>

<script>
import myHead from "./components/myHead.vue";
import myInput from "./components/myInput.vue";
import quoteContainer from "./components/quoteContainer";
import myFooter from "./components/myFooter.vue";

export default {
  name: "app",
  components: {
    myHead,
    myInput,
    quoteContainer,
    myFooter
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
