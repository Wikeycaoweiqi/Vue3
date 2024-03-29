<template>
  <div class="app">
    <h1>Hello Vue3</h1>
    <Person/>
  </div>
</template>

<script lang='js'>
import Person from "./components/1_import_component.vue"
export default {
  name: "App",
  components: {Person}
}
</script>

<style scoped>
.app {
  background-color: #ddd;
  box-shadow: 0 0 10px;
  border-radius: 10px;
  padding: 20px;
}
</style>