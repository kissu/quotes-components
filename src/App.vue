<template>
    <div class="container">
        <p class='text-center bg-primary'>This is main App</p>
        <br>
        <div class="progress">
          <div class="progress-bar progress-bar-striped active"
            aria-valuenow='30' aria-valuemin='0' aria-valuemax='100'
            :style="quotesPercentage">
            {{ quotes.length * 10 }}%
          </div>
        </div>

        <app-new-quote @quoteAdded='newQuote'></app-new-quote>
        <hr>
        {{ quotesPercentage }}
        <app-quote-grid :quotes="quotes" @quoteDeleted='deleteQuote'></app-quote-grid>
        <br>

        <div class="row">
          <div class="col-sm-12 text-center">
            <div class='alert alert-info'>
              Click on a Quote to delete it !
            </div>
          </div>

        </div>
    </div>
</template>

<script>
  import QuoteGrid from './components/QuoteGrid.vue'
  import NewQuote from './components/NewQuote.vue'

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
    methods: {
      newQuote(quote) {
        if (this.quotes.length > 9) {
          alert('You reached the limit of the quotes, delete some pls.')
        } else {
          this.quotes.push(quote)
        }
      },
      deleteQuote(index) {
        this.quotes.splice(index, 1)
      }
    },
    computed: {
      quotesPercentage() {
        return `width: ${this.quotes.length * 10}%`
      }
    },
    components: {
      appQuoteGrid: QuoteGrid,
      appNewQuote: NewQuote,
    }
  }
</script>

<style>
</style>
