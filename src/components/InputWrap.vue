<template>
  <form action="" @submit.prevent>
    <label for="">
      First Number :
      <input v-model="number1" type="text" name="first-number" id="" />
    </label>
    <label for="">
      Second Number :
      <input v-model="number2" type="text" name="second-number" id="" />
    </label>
    <div class="button-wrap">
      <Button text="+" @click="addNumbers" />
      <Button text="-" @click="subtractNumbers" />
      <Button text="÷" @click="divideNumbers" />
      <Button text="×" @click="multiplyNumbers" />
    </div>
  </form>
  <p>The result: {{ result }}</p>
</template>

<script setup lang="ts">
import Button from './Button.vue'
import { ref } from 'vue'

const number1 = ref<number>(0)
const number2 = ref<number>(0)
const result = ref<number>(0)

function addNumbers() {
  result.value = Number(number1.value) + Number(number2.value)
}
function multiplyNumbers() {
  result.value = Number(number1.value) * Number(number2.value)
}
function subtractNumbers() {
  result.value = Number(number1.value) - Number(number2.value)
}
function divideNumbers() {
  result.value = Number(number1.value) / Number(number2.value)
}
</script>

<style scoped>
input {
  width: 80px;
}
form {
  display: flex;
  gap: 10px;
  font-size: 20px;
}
.button-wrap {
  display: flex;
  flex-flow: column;
  gap: 10px;
}
p {
  display: block;
  padding: 10px;
  font-size: 20px;
}
</style>
