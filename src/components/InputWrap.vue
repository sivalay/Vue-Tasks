<template>
  <form action="">
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
      <active-button text="+" :onClick="addNumbers" />
      <active-button text="-" :onClick="subtractNumbers" />
      <active-button text="÷" :onClick="divideNumbers" />
      <active-button text="×" :onClick.stop="multiplyNumbers" />
    </div>
    <p>The result: {{ result }}</p>
  </form>
</template>

<script setup lang="ts">
import ActiveButton from './ActiveButton.vue'
import { computed, ref } from 'vue'

const number1 = ref<number>(0)
const number2 = ref<number>(0)
const result = ref<number>(0)

function addNumbers() {
  result.value = number1.value + number2.value
  console.log(result.value)
}
function multiplyNumbers() {
  result.value = number1.value + number2.value
  console.log(result.value)
}
function subtractNumbers() {
  result.value = number1.value + number2.value
  console.log(result.value)
}
function divideNumbers() {
  result.value = number1.value + number2.value
  console.log(result.value)
}

// const calculation = computed<number>(() => {
//   return result.value
// })
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
</style>
