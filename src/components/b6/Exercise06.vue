<template>
  <div>
    <h2>B6</h2>
    <h2>Shopping Cart</h2>
    <input type="number" v-model.number="inputValue" placeholder="Enter price" />
    <button @click="addToCart">Add to cart</button>
    <p>Current Input: {{ inputValue }}</p>
    <p>Total Price: {{ totalPrice }}</p>
  </div>
</template>

<script>
import { ref, computed } from 'vue';

export default {
  name: 'Exercise05',
  setup() {
    const inputValue = ref(0);
    const total = ref(0);
    const totalPrice = computed(() => total.value);
    const addToCart = () => {
      total.value += inputValue.value;
      inputValue.value = 0;
    };

    return {
      inputValue,
      totalPrice,
      addToCart
    };
  }
};
</script>
