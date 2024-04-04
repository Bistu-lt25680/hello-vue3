<template>
    <div class="Person">
        <h2>Car Info : A {{ car.brand }} car values : {{ car.price }} W</h2>
        <button @click="changePrice">Add 1 W</button>
        <hr>
        <h2>Game List : </h2>
        <ul>
            <li v-for="GamesInfo in games" :key="GamesInfo.id">
                {{ GamesInfo.name }}
            </li>
        </ul>
    </div>
</template >


<script lang="ts" setup>
    import { reactive } from 'vue'

    let car = reactive({
        brand:'Mercedes',
        price:(30),
    })

    let games = [
        {id:'2023010816',name:'CS1.6'},
        {id:'2023010817',name:'CSGO'},
        {id:'2023010818',name:'CS2'},
    ]

    function changePrice(){
        car.price+=1;
    }
</script>

<style scoped>
    .Person{
        background-color: aquamarine;
        box-shadow:0 0 10px;
        border-radius:10px;
        padding:20px;
    }
    button{
        margin:0 5px;
    }
</style>