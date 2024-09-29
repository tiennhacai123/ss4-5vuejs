<template>
  <div>
    <h2>B003</h2>

    <p v-if="userRole === 'admin'">Bạn có quyền quản trị.</p>
    <p v-else-if="userRole === 'user'">Bạn là người dùng bình thường.</p>
    <p v-else-if="userRole === 'guest'">Bạn là khách truy cập.</p>
    <p v-else>Vai trò không hợp lệ.</p>
  </div>
</template>

<script setup>
import { ref } from 'vue';
const userRole = ref('user'); 
</script>

<style scoped>
</style>
