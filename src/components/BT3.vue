<template>
  <div>
    <h2>Bài 3:</h2>
    <p>Diện tích: {{ acreage }}</p>
    <button @click="handleClick">change data</button>
  </div>
</template>

<script setup>
import { computed, ref } from "vue";

const width = ref(10);
const height = ref(20);
const acreage = computed(() => width.value * height.value);
const handleClick = () => {
  width.value += 10;
};
</script>

<style></style>
