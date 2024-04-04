<template>
    <div class="Person">
        <h2>姓名：{{name}}</h2> 
        <h2>年龄：{{age}}</h2>
        <button @click="changeName">修改姓名</button>
        <button @click="changeAge">修改年龄</button>
        <button @click="showTel">查看联系方式</button>
    </div>
</template >


<script lang="ts" setup name="Person">
    let name='刘天';            
    let age=18;                 
    let tel='13717980927';

    function changeName(){  
        if(name==='刘天'){
            name='Liu Tian'
        }else{
            name='刘天'
        }
    }

    function changeAge(){ 
        age+=1;
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