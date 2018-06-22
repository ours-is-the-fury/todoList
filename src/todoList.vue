<template>
  <div>
    <div>
      <input v-model="inputValue"/>
      <button @click="handleSubmit">tijiao</button>
    </div>
    <ul>
      <todo-item
      v-for=""
    </ul>
  </div>
</template>

<script>
import todoItem from'./components/todoItem'
export default{
  components:{
    'todo-item':todoItem
  },
  data (){
    return{
      inputValue:''
    }
  },
  methods:{
    handleSubmit(){
      this.list.push(this.inputValue)
      this.inputValue=''
    }
  }
}
</script>

<style>

</style>
