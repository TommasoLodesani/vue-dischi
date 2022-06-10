<template>
  <div>
   
  </div>
</template>

<script>

import axios from "axios";

export default {
  name: 'DiscList',
  components:{


  },
  data(){
    return{
        apiUrl : "https://flynn.boolean.careers/exercises/api/array/music",
        listaDischi :[]
    }
  },
  created(){
    this.getDischi();
    

  },
  methods: {
    getDischi(){
        axios.get(this.apiUrl)
        .then(result =>{
        this.listaDischi = result.data
        
    })

    }
  }
  
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

</style>
