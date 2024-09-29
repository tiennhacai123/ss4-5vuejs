<template>
  <div>
    <h2>B004</h2>

    <button @click="isVisible = true">Hiển thị</button>
    <button @click="isVisible = false">Ẩn</button>

    <p v-show="isVisible">Đây là thông báo được hiển thị!</p>
  </div>
</template>

<script setup>
import { ref } from 'vue';
const isVisible = ref(false);
</script>

<style scoped>
button {
  margin-right: 10px;
}
</style>
