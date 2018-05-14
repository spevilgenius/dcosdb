<script>
  import QuoteService from '../services/quote'

  export default {
    data () {
      return {
        quote: ""
      }
    },

    mounted () {
      QuoteService.getQuote(this).then(resp => {
        this.quote = resp.data[0].content
      }, (err) => {
        console.log(err)
      });
    }
  }
</script>

<template>
  <div>
    <div class="row">
      <div class="quote-wrapper">
        <h2>Random Quote</h2>
        <p>
          {{quote}}
        </p>
      </div>
    </div>
  </div>
</template>