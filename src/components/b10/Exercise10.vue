<template>
  <div>
    <h2>B10</h2>
    <button @click="showContent">Hiển thị</button>
    <button @click="hideContent">Ẩn</button>
    <p v-if="isVisible">Nội dung được hiển thị</p>
    <p v-else>Nội dung bị ẩn</p>
  </div>
</template>

<script>
import { ref } from 'vue';

export default {
  name: 'Exercise10',
  setup() {
    const isVisible = ref(false);

    const showContent = () => {
      isVisible.value = true;
    };

    const hideContent = () => {
      isVisible.value = false;
    };

    return {
      isVisible,
      showContent,
      hideContent
    };
  }
};
</script>

<style scoped>
button {
  margin-right: 10px;
}
</style>
