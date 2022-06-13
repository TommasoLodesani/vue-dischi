<template>
  <div>

    <MySelect @myselect="searchGenre"/>

    <section id="disc-container">
      <MyDisc v-for="(item,index) in filterListaDischi.response" :key="index"
      :discObject="item"/>
     
    </section>
  </div>
</template>

<script>

import axios from "axios";
import MyDisc from "./MyDisc.vue";
import MySelect from "./MySelect.vue";

export default {
  name: 'DiscList',
  components:{
    MyDisc,
    MySelect
},
  data(){
    return{
        apiUrl : "https://flynn.boolean.careers/exercises/api/array/music",
        listaDischi :[],
        userSelect: "",
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

    },
    searchGenre(selectUser){
      this.userSelect = selectUser;
      console.log(userSelect);

    },
    computed:{
      filterListaDischi(){
        return this.listaDischi;

        return this.listaDischi.filter(item =>{
          return item.response.genre
        })
      }
    }

  }
  
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
#disc-container{
    width: 70%;
    margin: auto;
    display: flex;
    flex-wrap: wrap;
}
</style>
