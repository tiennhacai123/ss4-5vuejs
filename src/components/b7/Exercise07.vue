<template>
  <div>
    <h2>B7</h2>
    <input type="number" v-model.number="number" placeholder="Enter a number" />
    <p>Current Number: {{ number }}</p>
    <p>Square of Number: {{ square }}</p>
  </div>
</template>

<script>
import { ref, computed, watch } from 'vue';

export default {
  name: 'Exercise07',
  setup() {
    const number = ref(0);

    const square = computed(() => number.value ** 2);

    watch(number, (newValue, oldValue) => {
      console.log(`Number changed from ${oldValue} to ${newValue}`);
    });

    return {
      number,
      square
    };
  }
};
</script>
