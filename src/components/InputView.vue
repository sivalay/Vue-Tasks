<template>
  <form action="">
    <label for="">
      First Number :
      <input v-model="number1" type="text" name="first-number" id="" />
    </label>
    <label for="">
      Second Number :
      <input v-model="number2" type="text" name="second-number" id="" />
    </label>
    <!-- <button-wrap /> -->
    <div class="button-wrap">
      <Button text="+" />
      <Button text="-" />
      <Button text="÷" />
      <Button text="×" />
    </div>
    <p>The first Value: {{ result }}</p>
  </form>
</template>

<script setup lang="ts">
// import ButtonWrap from './ButtonWrap.vue'
import Button from './Button.vue'
import { computed, ref } from 'vue'

const number1 = ref<number>(0)
const number2 = ref<number>(0)
const text = ref<string>('')
const result = ref<number>(0)

const calculation = computed<number>(() => {
  // console.log(result.value, 'Here is')
  return (result.value = 20)
  // switch
})
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
