<template>
  <main>
    <h1>Button Component</h1>
    <div class="button-container">
      <ButtonComponent text="Reply" icon="pi pi-angle-left" @click="msgPrinting" />
      <ButtonComponent text="Reply all" icon="pi pi-angle-double-left" @click="msgPrinting" />
      <ButtonComponent text="Forward" icon="pi pi-arrow-right" @click="msgPrinting" />
    </div>
  </main>
</template>

<script setup lang="ts">
import ButtonComponent from './components/ButtonComponent.vue'

function msgPrinting(text: string) {
  alert(`You've clicked the ${text} button`)
}
</script>

<style scoped>
.button-container {
  display: flex;
  gap: 10px;
  align-items: center;
}
</style>
