<template>
    <div>

        <select name="" id="" v-model="inputSelect" 
        @change="$emit('myselect',inputSelect)">
            <option value="">Rock</option>
            <option value="">Pop</option>
            <option value="">Jazz</option>
            <option value="">Metal</option>
        </select>
    </div>
</template>

<script>
export default {
  name: 'MySelect',
  data(){
    return{
        inputSelect: ""
    }
  }
  
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

</style>
