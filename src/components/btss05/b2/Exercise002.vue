<template>
  <div>
    <h2>B002</h2>

    <button @click="toggleShow">{{ isShow ? 'Hiện' : 'Ẩn' }}</button>
  </div>
</template>

<script setup>
import { ref } from 'vue';
const isShow = ref(false);

const toggleShow = () => {
  isShow.value = !isShow.value;
};
</script>

<style scoped>
button {
  margin-bottom: 10px;
}
</style>
