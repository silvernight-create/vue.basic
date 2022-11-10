<template>
  <div class="todo-header">
    <input type="text" placeholder="请输入你的任务名称，按回车确认" v-model="title" @keyup.enter="add()"/>

  </div>
</template>

<script>
import {nanoid} from 'nanoid'

export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: 'MyHeader',
  props:['receive'],
  data() {
    return {
      title:'',

    }
  },
  methods:{
    add(){
      if(!this.title.trim())  
      return alert('输入不能为空')
      const todoObj = {id:nanoid(),title:this.title,done:false}
      this.receive(todoObj)
      this.title = ''
      
    }
  },  
  

}
</script>
<style scoped>
.todo-header input{
  padding: 4px 7px;
  width: 560px;
  height: 28px;
  font-style: 14px;
  border: 1px solid #ccc;
  border-radius: 4px;
  
}
.todo-header input:focus{
  outline: none;
  border-color: rgba(82, 168,236, 0.8);
  box-shadow: inset 0 1px 1px rgba(0, 0,0 ,0.075),0 0 8px rgba(82, 168,236, 0.6);
}
</style>