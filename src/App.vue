<template>
    <div class="container">
        <p>This is main App parent</p>
        <app-quote-grid :quotes="quotes"></app-quote-grid>
    </div>
</template>

<script>
  import QuoteGrid from './components/QuoteGrid.vue'

  export default {
    data() {
      return {
        quotes: [
          "I'm a Potato ! :3",
          "Hello, me too ! :D"
        ],
        maxQuotes: 10
      }
    },
    components: {
      appQuoteGrid: QuoteGrid
    }
  }
</script>

<style>
</style>
