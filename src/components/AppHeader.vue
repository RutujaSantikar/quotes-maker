<template>
  <div class="row">
    <div class="col-sm-12">
        <div class="title-head">
        <h1>QCreator</h1>
        <p class="subtitle">Create meaningful quotes with QCreator</p>
        </div>
       
    <h4>Quotes Added</h4>
    <div class="progress">
        <div class="progress">
            <div class="progress-bar  progress-bar-striped" role="progressbar" aria-valuenow="60" aria-valuemin="0" aria-valuemax="100"
             :style="{width: (quoteCount / maxQuotes) *100 + '%'}">
              {{quoteCount}} / {{maxQuotes}}
            </div>
        </div>
    </div>
    </div>
  </div>
</template>

<script>
export default {
    name:'AppHeader',
    props:['quoteCount', 'maxQuotes']

}
</script>

<style scoped>
h1{
    font-weight: bold;
    color:#6638B7;
}
.subtitle{
    color: #29C0E6;
    font-size: 20px;
}
.title-head{
    padding: 10px 0px 15px 0px;
}
h4{
    color:#6638B7;
}
.progress-bar{
    background-color:#29C0E6;
}
</style>