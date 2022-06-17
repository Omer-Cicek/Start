<template>
  <div class="row">
    <app-quotes
      v-for="(quote, index) in quotes"
      @click.native="deleteQuote(index)"
      >{{ quote }}</app-quotes
    >
  </div>
</template>
<script>
import Quote from './Quote.vue';
export default {
  props: ['quotes'],
  components: {
    appQuotes: Quote,
  },
  methods: {
    deleteQuote(idx) {
      this.$emit('quoteDeleted', idx);
    },
  },
};
</script>

<style></style>
