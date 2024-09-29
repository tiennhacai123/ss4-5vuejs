<template>
  <div>
    <h2>B1</h2>
    <button @click="handleClick">Click duoc {{count}} lan</button>
  </div>
</template>

<script setup>
    import {ref} from 'vue'
    const count = ref(0);
    const handleClick = ()=>{
        count.value++;
    }
</script>

<style>

</style>