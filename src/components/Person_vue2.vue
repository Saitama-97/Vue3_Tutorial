<!--
  这是一个 Vue 2 组件：Person
  - 作用：展示一个人的姓名、年龄，并提供修改姓名、年龄的功能
  - 使用方式：直接引入并使用 <Person />
  - 事件交互：点击按钮修改数据（响应式）
-->
<template>
  <div class="person">
    <h2>姓名：{{ name }}</h2>
    <h2>年龄：{{ age }}</h2>
    <button @click="showTel">联系方式</button>
    <button @click="changeName">修改姓名</button>
    <button @click="changeAge">修改年龄</button>
  </div>
</template>

<script>
export default {
  name: 'person',
  data() {
    return {
      name: 'Alan',
      age: 28,
      phone: '13966668888',
    }
  },
  methods: {
    showTel() {
      alert(this.phone)
    },
    changeName() {
      this.name = 'Bob'
    },
    changeAge() {
      this.age += 1
    },
  },
}
</script>

<style>
.person {
  background-color: skyblue;
  box-shadow: 0 0 10px;
  border-radius: 10px;
  padding: 20px;
}
button {
  margin: 0 5px;
}
</style>
