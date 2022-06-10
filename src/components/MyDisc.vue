<template>
  <div class="disc">
    <img :src="discObject.poster" alt="">

   
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

</style>
