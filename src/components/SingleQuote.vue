<template>
  <div class="col-sm-6 col-md-4 col-lg-3">
     <div class="panel panel-default">
        <div class="panel-body quote" data-toggle="tooltip" data-placement="top" title="click on Quote to delete it !">
            <slot></slot>
        </div>
     </div>
     </div>
</template>

<script>
export default {
  name: 'SingleQuote',

  
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

.panel-body{
    font-size: 23px;
  
    
}
.quote{
    cursor: pointer;
    text-align: center;
    color:rgb(104, 103, 103);
}


</style>
