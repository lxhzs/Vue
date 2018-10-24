<template>
  <div id="app">
    <app-header v-bind:title="title" @changeTitData="updateTit($event)"></app-header>
    <hello v-bind:users="userArr"></hello>
    <hello v-bind:users="userArr"></hello>
    <app-footer v-bind:title="title"></app-footer>
  </div>
</template>

<script>

import Header from './components/Header'
import Hello from './components/Hello'
import Footer from './components/Footer'

export default {
    name: 'App',
    components: {
        "app-header": Header,
        "hello": Hello,
        "app-footer": Footer,
    },
    data(){
        return{
            userArr:[
                {name:"Levi",position:"web前端开发",show:false},
                {name:"Levi",position:"web前端开发",show:false},
                {name:"Levi",position:"web前端开发",show:false},
                {name:"Levi",position:"web前端开发",show:false},
                {name:"Levi",position:"web前端开发",show:false},
                {name:"Levi",position:"web前端开发",show:false},
                {name:"Levi",position:"web前端开发",show:false},
                {name:"Levi",position:"web前端开发",show:false},
                {name:"Levi",position:"web前端开发",show:false},
                {name:"Levi",position:"web前端开发",show:false},
            ],
            title: "传递的是一个值（string、number、boolean）",
        }

    },
    methods:{
        updateTit:function(tit){
            // tit 是子组件传过来的值
            this.title = tit;
        }
    }

}
</script>
  
<style scoped>
  /* h1{
    color: purple;
  } */
</style>
