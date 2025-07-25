<template>
  <button @click="number++">+</button>
  <p>
    {{ number }}
  </p>
</template>

<script setup>
import { ref, computed, reactive, watch } from 'vue'
const number = ref(0)

watch(number, (newval) => {
  if (newval % 2 == 0) {
    console.log('Even number detected')
  } else {
    console.log(newval)
  }
})
</script>

<style scoped></style>
