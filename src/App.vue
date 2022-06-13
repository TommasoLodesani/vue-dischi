<template>
  <div id="app">
    <MyHeader/>

   <main>
      <DiscList/>

    </main>
    
  </div>
</template>

<script>

import DiscList from './components/DiscList.vue'
import MyHeader from './components/MyHeader.vue'


export default {
  name: 'App',
  components: {
    DiscList,
    MyHeader,
}
}
</script>

<style lang="scss">
*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  // color: #2c3e50;
  // margin-top: 60px;

  main{
  background-color: #1e2d3b;
}
}
</style>
