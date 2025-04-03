<template>
  <!-- html -->
  <!-- 组件的结构 -->
  <div class="app">
    <!--    <h1>Hello</h1>-->
    <person></person>
  </div>
</template>

<script>
// JS & TS
import PersonVue2 from './components/Person_vue2.vue'

export default {
  name: 'App',
  components: { person: PersonVue2 },
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
