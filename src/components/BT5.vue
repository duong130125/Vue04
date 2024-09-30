<template>
  <div>
    <h1>Giỏ hàng</h1>
    <ul>
      <li v-for="cart in carts" :key="cart.id">
        {{ cart.name }} - số lượng {{ cart.quantity }}
        <button @click="handleClickIncrease(cart.id)">Tăng số lượng</button>
      </li>
    </ul>
    <p>Tổng số lượng sản phẩm: {{ total }}</p>
  </div>
</template>

<script setup>
import { ref, computed } from "vue";

const carts = ref([
  {
    id: 1,
    name: "cam",
    quantity: 3,
  },
  {
    id: 2,
    name: "xoài",
    quantity: 5,
  },
  {
    id: 3,
    name: "bưởi",
    quantity: 1,
  },
]);

const handleClickIncrease = (id) => {
  const cartItem = carts.value.find((cart) => cart.id === id);
  if (cartItem) {
    cartItem.quantity++;
  }
};

const total = computed(() => {
  return carts.value.reduce((acc, cart) => acc + cart.quantity, 0);
});
</script>

<style></style>
