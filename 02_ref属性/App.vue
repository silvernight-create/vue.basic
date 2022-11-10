<template>
  <div>
    <img src="./assets/logo.png" alt="logo">
    <h1 v-text="msg" ref="title"></h1>
    <button @click="showDOM()">点我输出上方DOM元素</button>
    <school/>
   
  </div>
  
</template>

<script>
import School from './components/School.vue'
    export default {
        name:'App',
        data() {
          return {
            msg:'欢迎学习Vue'
          }
        },
        components:{
          School
           
        },
        methods: {
          showDOM(){
            console.log(this.$refs.title)

          }
        },

    }
</script>


<style>

</style>
