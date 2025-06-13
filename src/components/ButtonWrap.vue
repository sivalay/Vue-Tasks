<template>
  <div class="button-wrap">
    <Button text="+" />
    <Button text="-" />
    <Button text="÷" />
    <Button text="×" />
  </div>
</template>

<script setup lang="ts">
import Button from './Button.vue'
</script>

<style scoped>
.button-wrap {
  display: flex;
  flex-flow: column;
  gap: 20px;
}
</style>
