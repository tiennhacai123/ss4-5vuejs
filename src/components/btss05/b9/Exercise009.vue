<template>
  <div>
    <h2>B009</h2>
    <p>Giới tính hiện tại: {{ currentGender }}</p>
    <button @click="randomGender">Random gender</button>
  </div>
</template>

<script setup>
import { ref } from 'vue';

const genders = ['Nam', 'Nữ', 'Khác'];
const currentGender = ref('Nam');

const randomGender = () => {
  const randomIndex = Math.floor(Math.random() * genders.length);
  currentGender.value = genders[randomIndex];
};
</script>
