<template>
  <div class="row">
    <form>
   <div class="col-sm-8 col-sm-offset-2 col-xs-12 col-md-6 col-md-offset-3 form-group">
    <div class="padding"></div>
    <textarea class="form-control quote-input" rows="3" v-model= "quote" placeholder= "Enter your quote here.."></textarea>
   </div>
   <div class="col-sm-8 col-sm-offset-2 col-xs-12 col-md-6 col-md-offset-3 form-group">
    <button class="btn btn-block" @click.prevent= "createNew" > Create Quote</button>
   </div>
    </form>
  </div>
</template>

<script>

export default {
  name: 'QuoteGrid',

 data: function(){
    return{
        quote:''
    };
 },
 methods:{
    createNew(){
        this.$emit( 'quoteAdded', this.quote);
        this.quote='';
    }
 }

  
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.btn{
    background-color: #6638B7;
    color:white ;
    padding: 10px;
    width: 70%;
    margin: 0 auto;
    
}
.padding{
    padding:20px;
}

</style>
