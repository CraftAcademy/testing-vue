<script setup>
import { ref } from "vue";

const x = ref(0);
const y = ref(0);

const handleMouseover = (event) => {
  x.value = event.offsetX;
  y.value = event.offsetY;
};
</script>

<template>
  <div v-on:mousemove="handleMouseover" class="box">
    {{ `x is: ${x}` }} – {{ `y is: ${y}` }}
  </div>
</template>

<style scoped>
.box {
  padding: 100px 0;
  width: 400px;
  text-align: center;
  background: #ddd;
  margin: 20px;
  display: inline-block;
}
</style>
