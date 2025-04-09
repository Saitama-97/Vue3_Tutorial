<template>
  <!-- html -->
  <!-- 组件的结构 -->
  <div class="app">
    <!--    <h1>Hello</h1>-->
    <person></person>
    <car></car>
  </div>
</template>

<script>
// JS & TS
// import PersonVue2 from './components/Person_vue2.vue'
import Person from './components/Person.vue'
import Car from './components/Car.vue'

export default {
  name: 'App',
  components: { person: Person, car: Car },
}
</script>

<!--<style>-->
<!--/* style */-->
<!--/* 组件的样式 */-->
<!--.app {-->
<!--  background-color: blanchedalmond;-->
<!--  box-shadow: 0 0 10px;-->
<!--  border-radius: 10px;-->
<!--  padding: 20px;-->
<!--}-->
<!--</style>-->
