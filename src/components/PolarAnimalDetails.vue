<script setup>
  defineProps({
    msg: String
  })
</script>

<template>
  <div>{{ msg }}</div>
  <slot></slot>
</template>

<style scoped></style>
