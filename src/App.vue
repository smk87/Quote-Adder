<template>
  <div class="container">
    <app-new-quote @quoteAdded="newQuote"></app-new-quote>
    <app-quote-grid :quotes="quotes" @quoteDelete="deleteQuote"></app-quote-grid>
    <div class="row">
      <div class="col-sm-12 text-center">
        <div class="alert alert-info">Info: Click on a Quote to delete it!</div>
      </div>
    </div>
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
    },
    deleteQuote(index) {
      this.quotes.splice(index, 1);
    }
  }
};
</script>

<style>
</style>
