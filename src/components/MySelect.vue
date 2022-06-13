<template>
    <div>

        <select name="" id="" v-model="inputSelect" 
        @change="swichSelect($event)">
            <option disabled value="">Scegli un genere</option>
            <option value="Rock">Rock</option>
            <option value="Pop">Pop</option>
            <option value="Jazz">Jazz</option>
            <option value="Metal">Metal</option>
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
  },
  methods: {
    swichSelect(event){
        this.inputSelect = event.target.value;
        this.$emit('myselect',this.inputSelect)
        console.log(this.inputSelect);
    }
  }
  
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

</style>
