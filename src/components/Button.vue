<template>
  <button @click="handleButtonClick">
    <i v-if="icon" :class="icon"></i>
    <span>{{ text }}</span>
  </button>
</template>

<script setup lang="ts">
const props = defineProps<{
  text: string
  icon: string
}>()

const emits = defineEmits<{
  (event: 'click', text: string): void
}>()

function handleButtonClick() {
  emits('click', props.text)
}
</script>

<style scoped>
button {
  display: flex;
  gap: 10px;
  font-size: 18px;
  color: lightslategray;
  border: 2px solid lightslategray;
  border-radius: 30px;
  padding: 10px 20px;
}
button:hover {
  background-color: #83adb9;
  border-color: #222;
  color: #fff;
}
</style>
