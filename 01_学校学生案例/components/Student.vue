<template>
<!-- 组件的结构 -->
    <div >
        <h2>学生名称：{{name}}</h2>
        <h2>学生年龄：{{age}}</h2>
        <button @click="showName()">点我提示学生名</button>
    
    </div>

</template>
<script>
//组件交互相关的代码

export default{
    
    // eslint-disable-next-line vue/multi-word-component-names
    name:'Student',
    data() {
        return {
            name:'张三',
            age:19
        }
    },
    methods: {
        showName(){
            alert(this.name)
    },
}
}
</script>


<!-- <style>
/* 组件的样式  */
.demo{
    background-color: orange;

}


</style> -->