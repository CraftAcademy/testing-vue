<script setup>
import { ref } from 'vue';

const firstName = ref('')
const handleSubmit = (event) => {
  debugger;
};
</script>

<template>
  <form @submit.prevent="handleSubmit">
    <input
      v-model="firstName"
      type="text"
      placeholder="Your Name"
    />
    <p> Input is {{ firstName }}</p>
    <input type="text" placeholder="Your favourite animal" />
    <button>Submit</button>
  </form>
</template>

<style scoped></style>
