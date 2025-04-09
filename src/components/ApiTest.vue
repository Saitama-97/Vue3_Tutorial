<template>
  <div class="p-4">
    <h2 class="text-xl font-bold mb-4">测试添加游泳池接口</h2>
    <button @click="testApi" class="bg-blue-500 text-white px-4 py-2 rounded hover:bg-blue-600">
      测试API
    </button>
    <div v-if="response" class="mt-4">
      <h3 class="font-semibold">返回结果：</h3>
      <pre class="bg-gray-100 p-2 rounded">{{ response }}</pre>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue'
import axios from 'axios'

const response = ref(null)

const testApi = async () => {
  try {
    const res = await axios.post('http://127.0.0.1:10810/web/swimmingPool/addPool/', {
      access_token:
        'eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJhdWQiOlsiYXBwIiwib2F1dGgyLXJlc291cmNlIiwid2ViIl0sInVzZXJfbmFtZSI6IjEzOTUyNjYxODkzIiwic2NvcGUiOlsiYWxsIl0sImV4cCI6MTc0NDE2NDY3NywiYXV0aG9yaXRpZXMiOlsiYXBwIiwid2ViIl0sImp0aSI6IjYwNDNhMzE4LTQwMGUtNDMyZi1hMjlkLTEyYjQwNjFkMjI5YyIsImNsaWVudF9pZCI6IndlYmFwcCIsIlgtQVVUSC1Vc2VySWQiOiJkMmExZThmNGJmMmM0MmM4ODAwMTIyNDExNWRlMWFiYSJ9.KNhRydT7zOMGYgiyfbMJUP0JAxmCGsbJTsHV_OrQQp0',
      poolName: '游泳池001',
    })

    response.value = JSON.stringify(res.data, null, 2)
  } catch (error) {
    response.value = `请求失败: ${error.message}`
  }
}
</script>

<style scoped>
pre {
  white-space: pre-wrap;
  word-break: break-word;
}
</style>
