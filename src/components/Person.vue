<template>
  <div class="person">
    <h2>姓名：{{ name }}</h2>
    <h2>年龄：{{ age }}</h2>
    <button @click="showTel">联系方式</button>
    <button @click="changeName">修改姓名</button>
    <button @click="changeAge">修改年龄</button>
  </div>
</template>

<!--<script>-->
<!--export default {-->
<!--  name: 'Person',-->
<!--  setup() {-->
<!--    // 数据-->
<!--    let name = 'Alan'-->
<!--    let age = 25-->
<!--    let tel = '13955558888'-->

<!--    // 方法-->
<!--    function showTel() {-->
<!--      alert(tel)-->
<!--    }-->

<!--    function changeName() {-->
<!--      name = 'Bob'-->
<!--      console.log(name)-->
<!--    }-->

<!--    function changeAge() {-->
<!--      age = 19-->
<!--      console.log(age)-->
<!--    }-->

<!--    return { name, age, changeAge, changeName, showTel }-->
<!--  },-->
<!--}-->
<!--</script>-->

<script setup name="Person">
// 创建基本类型的响应式数据
import { ref } from 'vue'

let name = ref('Alan')
let age = ref(25)
let tel = '13966668888'

function showTel() {
  alert(tel)
}

function changeName() {
  // ref定义的基本类型数据
  name.value = 'Bob'
}

function changeAge() {
  // ref定义的基本类型数据
  age.value = 28
}
</script>

<style></style>
