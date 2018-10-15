<template>
  <v-layout>
    <v-flex xs12 sm6 offset-sm3>
      <v-card class="margin">
        <v-card-title primary-title v-on:click="$emit('delQuote', numInArray)">
			<slot></slot>
        </v-card-title>
      </v-card>
    </v-flex>
  </v-layout>
</template>

<script>
export default {
  name: "quoteCard",
  props: ["numInArray"]
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.margin {
  margin: 10px;
}
</style>
