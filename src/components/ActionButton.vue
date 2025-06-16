<template>
  <button @click="handleClick">{{ text }}</button>
</template>

<script setup lang="ts">
const props = defineProps<{
  text: string
  onClick: () => void
}>()

const emits = defineEmits<{
  (event: 'click', text: string): void
}>()

function handleClick() {
  emits('click', props.text)
}
</script>

<style scoped>
button {
  cursor: pointer;
  padding: 5px 10px;
}
</style>
