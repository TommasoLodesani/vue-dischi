<template>
  <div class="disc">

    <img :src="discObject.poster" alt="">
    <div class="info">
        <h4> {{discObject.title}}</h4>
        <span> {{discObject.author}} </span><br>
        <span> {{discObject.year}} </span><br>

    </div>

  </div>
</template>

<script>



export default {
  name: 'MyDisc',
  props : {
    discObject : Object
  }
  
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

.disc{
    flex-basis: calc(100% / 6);
    margin: 10px;
    padding: 20px;
    padding-bottom: 30px;
    background-color: #2e3a46;

    img{
        max-width: 100%;
    }

    .info{
        padding-top: 10px;

        h4{
            color: white;
            text-transform: uppercase;
            margin-bottom: 10px;
        }

        span{
            
            color: #808077;
        }
    }

}


</style>
