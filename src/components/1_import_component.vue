<template>
  <div class="person">
    <h2>name: {{ name }}</h2>
    <h2>gender: {{ gender }}</h2>
    <button @click="showAge()">click to show age</button>
  </div>
</template>

<script lang='js'>
export default {
  name: 'Person',
  data() {
    return {
      name: 'zhangsan',
      age: '18',
      gender: 'male'
    }
  },
  methods: {
    showAge() {
      alert(this.age);
    }
  }
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