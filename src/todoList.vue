<template>
  <div><!--只能有一个包裹元素-->
    <div>
      <input  v-model = "inputValue" />
      <button @click = "handleSubmit">tijiao</button>
    </div>
    <ul>
      <todo-item 
      v-for= "(item , index) of list"
      :key = "index"
      :content = "item"
      :index= "index"
      @delete= "handleDelete" 
      ></todo-item>
    </ul>
  </div>
</template>

<script>
import todoItem from "./components/todoItem";
export default {
  components: {
    "todo-item": todoItem
  },
  data() {
    //以前是对象，现在应该是一个函数
    return {
      inputValue: "",
      list: []
    };
  },
  methods: {
    handleSubmit() {
      this.list.push(this.inputValue); //list 自动寻找list
      this.inputValue = "";
    },
    handleDelete (index){
      this.list.splice(index, 1)
    }
  }
};
</script>

<style>

</style>
