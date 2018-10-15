<template>
	<div>
		<v-flex xs12>
        <v-textarea
          solo
		  v-model="quote"
          name="input-7-4"
          label="Enter your quote here..."
        ></v-textarea>
		<v-btn color="info" v-on:click="$emit('newQuote', quote)">Add Quote</v-btn>
      </v-flex>
	</div>
</template>

<script>
export default {
  name: "myInput",
  data: function() {
    return {
      quote: ""
    };
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
