<template>
  <div>
    <h2>Bài 2:</h2>
    <p>Company: {{ object.company }}</p>
    <p>Company: {{ object.age }}</p>
    <button @click="handleChange">Change data</button>
  </div>
</template>

<script setup>
import { reactive } from "vue";
const object = reactive({
  company: "Rikkei Academy",
  age: 2,
});
const handleChange = () => {
  (object.company = "Rikkei Education"), (object.age = 1);
};
</script>

<style></style>
