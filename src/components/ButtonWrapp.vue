<template>
  <h1>Button Component</h1>
  <div class="button-container">
    <Button text="Reply" icon="pi pi-angle-left" @click="handleAlert" />
    <Button text="Reply all" icon="pi pi-angle-double-left" @click="handleAlert" />
    <Button text="Forward" icon="pi pi-arrow-right" @click="handleAlert" />
  </div>
</template>

<script setup lang="ts">
import Button from './Button.vue'

function handleAlert(text: string) {
  alert(`You've clicked the '${text}' button`)
}
</script>

<style scoped>
.button-container {
  display: flex;
  gap: 10px;
  align-items: center;
}
</style>
