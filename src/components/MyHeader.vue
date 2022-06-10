<template>
  <header>
    <img src="../assets/img/logo-small.svg" alt="">
  </header>
</template>

<script>
export default {
  name: 'MyHeader',
  
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
header{
    width: 100%;
    height: 45px;
    background-color: #2e3a46;
    display: flex;
    justify-content: flex-start;
    align-items: center;

    img{
        width: 30px;
        margin-left: 20px;
    }
}

</style>
