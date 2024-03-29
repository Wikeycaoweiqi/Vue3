<template>
  <div class="person">
    <h2>name: {{ name }}</h2>
    <button @click="changeName()">click to change name</button>
    <h2>gender: {{ gender }}</h2>
    <h2>age: {{ age }}</h2>
    <button @click="showAge()">click to show age</button>
    <button @click="changeAge()">click to change age</button>
  </div>
</template>

<script lang="js">
export default {
  name: 'Person1'
}
</script>

<script lang='js' setup>
let name = 'zhangsan';
let age = '18';
let gender = 'male';

function changeName() {
  name = 'lisi';
}

function showAge() {
  alert(age);
}

function changeAge() {
  age += 1;
}
</script>

<style scoped>
.person {
  background-color: skyblue;
  box-shadow: 0 0 10px;
  border-radius: 10px;
  padding: 20px;
}
</style>