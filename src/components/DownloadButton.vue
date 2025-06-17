<template>
  <div class="download-button-wrap">
    <Button icon="pi pi-arrow-down" class-name="download-button" @click="showAlertMessage" />
  </div>
</template>

<script setup lang="ts">
import Button from './Button.vue'

function showAlertMessage() {
  alert(`You've clicked the Download button`)
}
</script>

<style scoped>
.download-button-wrap {
  margin-top: 50px;
}
.download-button {
  color: red;
  border-radius: 10px;
  gap: 0px;
}
</style>
