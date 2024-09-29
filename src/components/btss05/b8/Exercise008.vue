<template>
  <div>
    <h2>B008</h2>
    <button @click="sortAscending">Tăng dần</button>
    <button @click="sortDescending">Giảm dần</button>
    <ul>
      <li v-for="(number, index) in numbers" :key="index">{{ number }}</li>
    </ul>
  </div>
</template>

<script setup>
import { ref } from 'vue';

const numbers = ref([5, 3, 8, 1, 4]);

const sortAscending = () => {
  numbers.value.sort((a, b) => a - b);
};

const sortDescending = () => {
  numbers.value.sort((a, b) => b - a);
};
</script>
