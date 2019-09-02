<template>
  <div class="row">
    <app-quote v-for="(quote,index) in quotes" @click.native="deleteQuote(index)">{{quote}}</app-quote>
  </div>
</template>

<script>
import QuoteVue from "./Quote.vue";

export default {
  props: ["quotes"],
  components: {
    appQuote: QuoteVue
  },
  methods: {
    deleteQuote(index) {
      this.$emit("quoteDelete", index);
    }
  }
};
</script>

<style>
</style>