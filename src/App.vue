<template>
  <div class="container">
    <app-quote-grid :quotes="quotes"></app-quote-grid>
  </div>
</template>

<script>
import QuoteGridVue from "./components/QuoteGrid.vue";

export default {
  data() {
    return {
      quotes: ["Just a quote to see something."],
      maxQuotes: 10
    };
  },
  components: {
    appQuoteGrid: QuoteGridVue
  }
};
</script>

<style>
</style>
