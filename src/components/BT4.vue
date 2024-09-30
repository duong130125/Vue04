<template>
  <div>
    <h2>Bài 4:</h2>
    <input type="text" v-model="indexValue" @change="handleChange" />
  </div>
</template>

<script setup>
import { ref, watch } from "vue";

const indexValue = ref("");

const handleChange = (e) => {
  indexValue.value = e.target.value;
};

watch(indexValue, (newValue, oldValue) => {
  console.log(`Giá trị thay đổi từ "${oldValue}" thành "${newValue}"`);
});
</script>

<style></style>
