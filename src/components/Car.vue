<template>
  <div class="car">
    <h2>一辆{{ car.brand }}车，价值{{ car.price }}</h2>
    <button @click="changeBrand">修改品牌</button>
    <button @click="changePrice">修改价格</button>
    <hr />
    <h2>游戏列表：</h2>
    <ul>
      <li v-for="g in games" v-bind:key="g.id">{{ g.name }}</li>
    </ul>
    <button @click="changeFirstGame">修改第一个游戏名称</button>
    <hr />
    <h2>C：{{ obj.a.b.c }}</h2>
    <button @click="changeC">修改C</button>
  </div>
</template>

<script setup name="Car">
// 创建复杂类型（如对象）的响应式数据
import { reactive } from 'vue'

// 数据
let car = reactive({ brand: '大众', price: 20 })

let games = reactive([
  { id: '001', name: 'Dota2' },
  { id: '002', name: 'CS2' },
  { id: '003', name: 'HeartStone' },
])

let obj = reactive({ a: { b: { c: 666 } } })

// 方法
function changeBrand() {
  car.brand = '丰田'
}

function changePrice() {
  car.price += 10
}

function changeFirstGame() {
  games[0].name = 'Overwatch'
}

function changeC() {
  obj.a.b.c = 999
}
</script>

<style></style>
