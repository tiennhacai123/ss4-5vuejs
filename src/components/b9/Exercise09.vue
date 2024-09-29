<template>
  <div>
    <h2>B9</h2>
        <div v-for="product in products" :key="product.id" class="product">
      <h3>{{ product.title }}</h3>
      <p><strong>Author:</strong> {{ product.author }}</p>
      <p>{{ product.content }}</p>
      <hr />
    </div>
  </div>
</template>

<script>
import { ref } from 'vue';

export default {
  name: 'Exercise09',
  setup() {
    const products = ref([
      { id: 1, title: 'Vue.js Basics', content: 'An introduction to Vue.js framework.', author: 'John Doe' },
      { id: 2, title: 'Advanced Vue Techniques', content: 'Learn advanced techniques for building apps with Vue.', author: 'Jane Smith' },
      { id: 3, title: 'State Management with Vuex', content: 'Manage your application state efficiently using Vuex.', author: 'Alice Johnson' },
    ]);

    return {
      products
    };
  }
};
</script>

<style scoped>
.product {
  margin-bottom: 20px;
}
</style>
