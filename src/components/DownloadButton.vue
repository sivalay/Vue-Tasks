<template>
  <div class="download-wrap">
    <Button
      text=""
      icon="pi pi-arrow-down"
      class-name="text-col border-raduis"
      @click="showAlertMessage"
    />
  </div>
</template>

<script setup lang="ts">
import Button from './Button.vue'

function showAlertMessage(text: string) {
  alert(`You've clicked the ${text} button`)
}
</script>

<style scoped>
.download-wrap {
  margin-top: 50px;
}
.text-col {
  color: red;
}
.border-raduis {
  border-radius: 10px;
}
button {
  gap: 0px;
}
</style>
