<template>
  <div class="row">
   <app-quote v-for= "(quote , index ) in quotes" :key= "quote.id" @click.native= "deleteQuote(index)"> <sup><i class="fas fa-quote-left"></i></sup> {{quote}} <sup><i class="fas fa-quote-right"></i></sup></app-quote>
  </div>
</template>

<script>
import SingleQuote from './SingleQuote.vue';
export default {
  name: 'QuoteGrid',

props:['quotes'],
components:{
  appQuote:SingleQuote
},

  methods:{
    deleteQuote(index){
      this.$emit('quoteDeleted', index);

    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.fas{
  font-size: 15px;
 
}
.fa-quote-right{
  color:#99CCED;
}
.fa-quote-left{
color: #9C89FF;
}
</style>
