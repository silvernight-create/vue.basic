<template>
  <div>
    <ul class="todo-main"> 
    <MyItem 
      v-for="todoObj in todos" :key="todoObj.id" 
      :todo="todoObj" 
     
      />
    </ul>

  </div>
</template>

<script>
import MyItem from './MyItem.vue'


export default {
  
  
  // eslint-disable-next-line vue/multi-word-component-names
  name: 'MyList',
  data() {
    return {
      
    }
  },
  components:{
    MyItem,
 
  },
  props:['todos']
     
  

}
</script>
<style scoped>
.todo-main{
  margin-left: 0px;
  border: 1px solid #ddd;
  border-radius: 2px;
  padding: 0px;
}
.todo-empty{
  height:40px;
  line-height: 40px;
  border: 1px solid #ddd;
  border-radius: 2px;
  padding-left: 5px;
  margin-top: 10px;

}
</style>