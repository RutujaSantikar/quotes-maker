<template>
<div id="app">
  <div class="container">
    <app-header :quoteCount= " quotes.length" :maxQuotes= "maxQuotes"></app-header>
     <app-new-quote @quoteAdded= " newQuote"></app-new-quote>
    <app-quote-grid :quotes= "quotes" @quoteDeleted= "deleteQuote" ></app-quote-grid> 
  </div>
</div>
</template>

<script>
import QuoteGrid from './components/QuoteGrid.vue'
import NewQuote from './components/NewQuote.vue'
import AppHeader from './components/AppHeader.vue'

export default {
  name: 'App',
  data : function () {
    return {
      quotes:[ ],
      maxQuotes:15
    };
    

  },
 methods:{
  newQuote(quote){
    if(this.quotes.length >= this.maxQuotes){
      return alert ('Please delete previous Quotes to add new')
      
    }
    this.quotes.push(quote);
  },
  deleteQuote(index){
    this.quotes.splice(index,1);
  }
 },
  components: {
    appQuoteGrid:QuoteGrid,
    appNewQuote:NewQuote,
    appHeader:AppHeader
  }
}
</script>

<style scoped>
#app{
  width:90%;
  margin: 0 auto;

}

</style>
