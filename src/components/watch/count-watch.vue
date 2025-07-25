<template>
  <button @click="count++">Click</button>
  <p>
    {{ count }}
  </p>
</template>

<script setup>
import { ref, computed, reactive, watch } from 'vue'

const count = ref(0)

watch(count, (newVal, oldVal) => {
  console.log(`The count changed from ${oldVal} to ${newVal}`)
})
</script>

<style scoped></style>
