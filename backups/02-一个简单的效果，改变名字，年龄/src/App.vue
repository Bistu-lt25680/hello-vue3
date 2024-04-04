<template>
    <div id="App">
        <h1>Hello Vue3!</h1>
        <Person/>
    </div>
</template>

<script>
    import Person from './components/Person.vue'
    export default {
        name: 'App',     //组件名
        components: {     //注册组件
            Person
        }
    }
</script>

<style>
    #App{
        background-color: #ddd;
        box-shadow:0 0 10px;
        border-radius:10px;
        padding:20px;
    }
</style>