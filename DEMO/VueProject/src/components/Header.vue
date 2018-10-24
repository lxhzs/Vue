<template>
    <header class="app-header" v-on:click="changeTit">
        <h1>{{title1}} {{title}}</h1>
    </header>
</template>

<script>
    export default {
        name: "app-header",
        data(){
            return{
                title1: "Vue.js Demo",
            }
        },
        props:{
            title:{
                type: String,
                required: true
            }
        },
        methods:{
            changeTit:function(){
                // 1-这里只是做展示效果作用，直接在子组件内修改父组件属性值不满足vue的单项数据流
                // this.title = "has be changed!";  

                // 2-可以通过事件传值，将子传到父
                this.$emit('changeTitData','son change father');
            }
        }
    }
</script>

<style scoped>
    header{
        background: lightseagreen;
        padding: 10px;
    }
    h1{
        color: #fff;
        text-align: center;
    }
</style>
