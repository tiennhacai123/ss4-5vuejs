<template>
  <div>
    <h2>B4</h2>
    <input @input="handleInput" type="text">
  </div>
</template>

<script setup>
    import {ref, watch} from 'vue'
    let inputValue = ref("");
    const handleInput = (event) =>{
        inputValue.value = event.target.value;  
        watch(inputValue,(newtext,oldText)=>{
            console.log(`gia tri thay doi tu ${oldText} thanh ${newtext}`);
        })
    }

</script>

<style>

</style>