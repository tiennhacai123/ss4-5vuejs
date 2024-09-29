<template>
  <div>
    <h2>B005</h2>

    <ul>
      <li v-for="(number, index) in evenNumbers" :key="index">{{ number }}</li>
    </ul>
  </div>
</template>

<script setup>
import { ref, computed } from 'vue';

const numbers = ref([1, 2, 3, 4, 5, 6, 7, 8, 9, 10]);

const evenNumbers = computed(() => {
  return numbers.value.filter(number => number % 2 === 0);
});
</script>

<style scoped>
ul {
  list-style-type: none;
  padding: 0;
}
li {
  margin: 5px 0;
}
</style>
