<template>
  <div>
    <h2>B3</h2>
    <p>Acreage: {{ Acreage }}</p>
    <button @click="handleChange">Change Data</button>
  </div>
</template>

<script setup>
import { ref, computed } from "vue";
const width = ref(10); //{value=10}
const height = ref(20);
let Acreage = computed(() => width.value * height.value);

const handleChange = () => {
  width.value = 20;
  Acreage = width.value * height.value;
};
</script>

<style></style>
