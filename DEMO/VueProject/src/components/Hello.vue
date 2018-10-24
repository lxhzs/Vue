<template>
    <div class="hello">
        <h1>Hello EveryOne</h1>
        <ul>
            <li v-for="user in users" @click="user.show = !user.show">
                <h2>{{user.name}}</h2>
                <h3 v-show="user.show">{{user.position}}</h3>
            </li>
        </ul>
        <button @click="deleteArr()">删除</button>
    </div>
</template>

<script>
    export default{
        name: 'hello',
        props:{
            users:{
                type:Array,
                required: true,
            }
        },
        data(){
            return{
              
            }
        },
        methods:{
            deleteArr:function(){
                this.users.pop();
            }
        }
    }
</script>

<style scoped>
    .hello{
        width: 100%;
        max-width: 1200px;
        margin: 40px auto;
        padding: 0 20px;
        box-sizing: border-box;
    }
    ul{
        display: flex;
        flex-wrap: wrap;
        list-style: none;
        padding: 0;
    }
    li{
        flex-grow: 1;
        flex-basis: 300px;
        text-align: center;
        padding: 30px;
        border: 1px solid #222;
        margin: 10px;
    }
</style>
