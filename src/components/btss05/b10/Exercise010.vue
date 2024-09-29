<template>
  <div>
    <h2>B010</h2>
    <button @click="addRandomNumber">Random number</button>
    <ul>
      <li v-for="(number, index) in numbers" :key="index">{{ number }}</li>
    </ul>
  </div>
</template>

<script setup>
import { ref } from 'vue';

const numbers = ref([]);

const addRandomNumber = () => {
  const randomNumber = Math.floor(Math.random() * 100); 
  numbers.value.push(randomNumber);
};
</script>
