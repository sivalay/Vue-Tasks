<template>
  <button @click="handleButtonClick">{{ text }}</button>
</template>

<script setup lang="ts">
const props = defineProps<{
  text: string
}>()

const emits = defineEmits<{
  (event: 'click'): void
}>()

function handleButtonClick() {
  emits('click')
}
</script>

<style scoped>
button {
  cursor: pointer;
  padding: 5px 10px;
}
</style>
