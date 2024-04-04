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
        data() {
            return{
                name: '刘天',
                age: 18,
                tel:'13717980927'
            }
        },
        methods: {
            showTel() {
                alert(this.tel)
            },
            changeName() {
                if(this.name === '刘天')
                    this.name = 'Liu Tian'
                else
                    this.name = '刘天'
            },
            changeAge() {
                this.age += 1 
            },
        }
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