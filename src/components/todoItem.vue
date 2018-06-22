<template>
<li class="item" @click="handleDelete">{{content}}</li>
</template>

<script>
export default{
    props: ['content','index'], //接收数据定义
    methods:{
        handleDelete(){
            this.$emit('delete',this.index)
        }
    }
}
</script>


<style scoped> /*scoped 定义局部作用域*/
.item{
    color: green 
}

</style>
