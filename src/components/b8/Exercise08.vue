<template>
  <div>
    <h2>B8</h2>
    <ul v-for="product in products" :key="product.id">
      <li>
        {{ product.name }} - So luong: {{ product.quantity }}
        <button @click="handleClick(product)">Tang so luong</button>
      </li>
    </ul>
    <p>Tong so luong: {{ totalQuantity }}</p>
  </div>
</template>

<script setup>
import { reactive, computed } from "vue";
const products = reactive([
  {
    name: "Men men loai 1",
    quantity: 3,
  },
  {
    name: "Men men loai 2",
    quantity: 5,
  },
  {
    name: "Men men loai 3",
    quantity: 1,
  },
]);
const handleClick = (product) => {
  product.quantity++;
};
const totalQuantity = computed(() => {
  return products.reduce((total, product) => total + product.quantity, 0);
});
</script>

<style></style>
