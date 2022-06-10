<template>
  <section>
    <MyDisc v-for="(item,index) in listaDischi.response" :key="index"
    :discObject="item"/>
   
  </section>
</template>

<script>

import axios from "axios";
import MyDisc from "./MyDisc.vue";

export default {
  name: 'DiscList',
  components:{
    MyDisc
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
