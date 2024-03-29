<template>
  <div class="person2">
    <h2>name: {{ name }}</h2>
    <button @click="changeName()">click to change name</button>
    <h2>gender: {{ gender }}</h2>
    <h2>age: {{ age }}</h2>
    <button @click="showAge()">click to show age</button>
    <button @click="changeAge()">click to change age</button>
  </div>
</template>

<script lang="js">
import {ref} from 'vue';

export default {
  name: 'Person2'
}
</script>

<script lang='js' setup>
let name = ref('Lily');
let age = ref(20);
let gender = 'female';

function changeName() {
  name.value = 'Lucy';
}

function showAge() {
  alert(age.value);
  console.log(age);
}

function changeAge() {
  age.value += 1;
}
</script>

<style scoped>
.person2 {
  background-color: pink;
  box-shadow: 0 0 10px;
  border-radius: 10px;
  padding: 20px;
}
</style>