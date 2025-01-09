<template>
  <div class="person">
    <h2>姓名：{{ name }}</h2>
    <h2>年龄：{{ age }}</h2>
    <button @click="changeName">修改名称</button>
    <button @click="changeAge">修改年龄</button>
    <button @click="showTel">查看联系方式</button>
  </div>
</template>

<script lang="ts">
export default {
  name: 'Person',
}
</script>

<script lang="ts" setup>
import { ref } from 'vue'
let name = ref('张三')
let age = ref(18)
let tel = '1233546678'
let address = 'shanghaijinqinyuan'
console.log(name)
console.log(address)
function changeName() {
  name.value = 'daiyouli'
}
function changeAge() {
  age.value += 1
}
function showTel() {
  alert(tel)
}
</script>

<style scoped>
.person {
  background-color: cadetblue;
  box-shadow: 0 0 10px;
  border-radius: 10px;
  padding: 20px;
}
</style>
