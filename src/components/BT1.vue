<template>
  <div>
    <h2>Bài 1:</h2>
    <button @click="handleClick">Click {{ count }} lần</button>
  </div>
</template>

<script setup>
import { ref } from "vue";
const count = ref(0);
const handleClick = () => {
  count.value++;
};
</script>

<style></style>
