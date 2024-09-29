<template>
  <div>
    <h2>B2</h2>
    <ul>
      <li>Company: {{userInfo.Company}}</li>
      <li>Age: {{userInfo.Age}}</li>
    </ul>
    <button @click="handleChange">Change Data</button>
  </div>
</template>

<script setup>
import { reactive } from "vue";
const userInfo = reactive({
  Company: "Rekkei Academy",
  Age: 2,
});
console.log(userInfo);

const handleChange = () => {
  (userInfo.Company = "Rekkei Education"), (userInfo.Age = 1);
};
</script>

<style></style>
