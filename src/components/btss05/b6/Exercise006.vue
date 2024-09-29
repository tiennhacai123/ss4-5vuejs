<template>
  <div>
    <h2>B006</h2>
    <ul>
      <li v-for="(number, index) in evenNumbers" :key="index">{{ number }}</li>
    </ul>
  </div>
</template>

<script setup>
import { ref, computed } from 'vue';

const numbers = ref([12, 3, 5, 8, 7, 10, 14, 1]); 
const evenNumbers = computed(() => {
  return numbers.value.filter(number => number % 2 === 0);
});
</script>
