<template>
    <div class="Person">
        <h2>姓名：{{name}}</h2> 
        <h2>年龄：{{age}}</h2>
        <button @click="changeName">修改姓名</button>
        <button @click="changeAge">修改年龄</button>
        <button @click="showTel">查看联系方式</button>
    </div>
</template >

<script>
    export default {
        name: 'Person',
        setup() {//setup函数里的this指向undefined
            //数据

            let name='刘天';            //name不是响应式数据
            let age=18;                 //age不是响应式数据
            let tel='13717980927';

            //方法
            function changeName(){  //这样修改name不更新，但确实改了
                if(name==='刘天'){
                    name='Liu Tian'
                }else{
                    name='刘天'
                }
            }

            function changeAge(){ //这样修改age不更新，但确实改了
                age+=1;
            }

            function showTel(){
                alert(tel)
            }

            return {name,age,changeName,changeAge,showTel}
        },
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