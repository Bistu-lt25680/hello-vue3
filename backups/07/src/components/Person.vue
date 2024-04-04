<template>
    <div class="Person">
        <h2>姓名：{{name}}</h2> 
        <h2>年龄：{{age}}</h2>
        <h2>地址：{{address}}</h2>
        <button @click="changeName">修改姓名</button>
        <button @click="changeAge">修改年龄</button>
        <button @click="showTel">查看联系方式</button>
    </div>
</template >


<script lang="ts" setup>
    import { ref } from 'vue'

    let name = ref('刘天');            
    let age = ref(18);                 
    let tel = '13717980927';
    let address = '北京市昌平区太行路55号北京信息科技大学新校区';

    function changeName(){  
    if(name.value === '刘天'){
        name.value = 'Liu Tian';
    }else{
        name.value = '刘天';
    }
}


    function changeAge(){ 
        age.value+=1;
    }

    function showTel(){
        alert(tel)
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