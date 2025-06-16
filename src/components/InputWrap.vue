<template>
  <form action="" @submit.prevent>
    <label for="">
      First Number :
      <input v-model="number1" type="number" name="first-number" id="" />
    </label>
    <label for="">
      Second Number :
      <input v-model="number2" type="number" name="second-number" id="" />
    </label>
    <!-- <button-wrap /> -->
    <div class="button-wrap">
      <action-button text="+" :onClick="addNumbers" />
      <action-button text="-" :onClick="subtractNumbers" />
      <action-button text="÷" :onClick="divideNumbers" />
      <action-button text="×" :onClick="multiplyNumbers" />
    </div>
  </form>
  <p>The result: {{ result }}</p>
</template>

<script setup lang="ts">
import ActionButton from './ActionButton.vue'
import { ref } from 'vue'

const number1 = ref<number>(0)
const number2 = ref<number>(0)
const result = ref<number>(0)

function addNumbers() {
  result.value = number1.value + number2.value
  console.log(result.value)
}
function multiplyNumbers() {
  result.value = number1.value * number2.value
  console.log(result.value)
}
function subtractNumbers() {
  result.value = number1.value - number2.value
  console.log(result.value)
}
function divideNumbers() {
  result.value = number1.value / number2.value
  console.log(result.value)
}
</script>

<style scoped>
input {
  width: 80px;
}
form {
  display: flex;
  gap: 10px;
}
.button-wrap {
  display: flex;
  flex-flow: column;
  gap: 10px;
}
p {
  display: block;
  padding: 10px;
}
</style>
