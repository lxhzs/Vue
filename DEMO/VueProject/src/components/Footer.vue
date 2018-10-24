<template>
    <footer class="app-footer">
        <p>{{copyright}} {{title}}</p>
    </footer>
</template>

<script>
    export default {
        name:"app-footer",
        data () {
            return {
                copyright: "copyright 2018 vue.js",
            }
        },
        props:{
            title:{
                type: String
            }
        }
    }
</script>

<style scoped>
    footer{
        background: #222;
        padding: 6px;
    }
    p{
        color: lightgreen;
        text-align: center;
    }
</style>