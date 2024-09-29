<template>
  <div>
    <h2>B001</h2>

    <button @click="isShow = true">Hiển thị nội dung</button>

    <p v-if="isShow">Rikkei Education</p>
  </div>
</template>

<script setup>
import { ref } from 'vue';
const isShow = ref(false);
</script>

<style scoped>
button {
  margin-bottom: 10px;
}
</style>
