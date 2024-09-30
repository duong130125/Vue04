<template>
  <div>
    <input type="number" v-model.number="inputNumber" />
    <button @click="handleClickAddCart">Add to cart</button>
    <p>Tổng tiền trong giỏ hàng: {{ total }}</p>
  </div>
</template>

<script setup>
import { ref } from "vue";

const inputNumber = ref(0);
const total = ref(0);

const handleClickAddCart = () => {
  total.value += Number(inputNumber.value);
  inputNumber.value = 0;
};
</script>

<style></style>
