<template>
  <div class="car">
    <h2>car brand: {{ car.brand }}</h2>
    <h2>car price: {{ car.price }}</h2>
    <button @click="changePrice()">click to change price</button>
    <h2>car list:</h2>
    <ul>
      <li v-for="car in carList" :key="car.brand">{{ car.brand }} {{ car.price }}</li>
    </ul>
    <button @click="changeFirstCarPrice()">change first car price</button>
  </div>
</template>

<script lang="js">
export default {
  name: 'Car2'
}
</script>

<script lang='js' setup>
import {ref} from "vue";

let car = ref({
  brand: 'benz',
  price: 100
})
let carList = ref([
  {brand: "bmw", price: 100},
  {brand: "byd", price: 80},
  {brand: "audi", price: 50},
])

function changePrice() {
  car.value.price += 10;
}

function changeFirstCarPrice() {
  carList.value[0].price += 10;
}
</script>

<style scoped>
.car {
  background-color: cornflowerblue;
  box-shadow: 0 0 10px;
  border-radius: 10px;
  padding: 20px;
}

li {
  font-size: 20px;
}
</style>