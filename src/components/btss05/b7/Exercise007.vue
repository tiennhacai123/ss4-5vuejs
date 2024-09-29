<template>
  <div>
    <h2>B007</h2>
    <button
      v-for="index in 3"
      :key="index"
      @click="activeIndex = index"
      :class="{ active: activeIndex === index }"
    >
      Button {{ index }}
    </button>
  </div>
</template>

<script setup>
import { ref } from 'vue';

const activeIndex = ref(1);
</script>

<style scoped>
button {
  margin-right: 10px;
}

.active {
  background-color: red;
  color: #fff;
}
</style>
