<template>
  <div class="container">
    <app-new-quote @quoteAdded="newQuote"></app-new-quote>
    <app-quote-grid :quotes="quotes"></app-quote-grid>
  </div>
</template>

<script>
import QuoteGridVue from "./components/QuoteGrid.vue";
import NewQuoteVue from "./components/NewQuote.vue";

export default {
  data() {
    return {
      quotes: ["Just a quote to see something."],
      maxQuotes: 10
    };
  },
  components: {
    appQuoteGrid: QuoteGridVue,
    appNewQuote: NewQuoteVue
  },
  methods: {
    newQuote(quote) {
      this.quotes.push(quote);
    }
  }
};
</script>

<style>
</style>
