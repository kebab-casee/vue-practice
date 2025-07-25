<template>
  <p>
    Input box color:
    <input type="text" v-model="color" />
  </p>
  <p>
    Input box size:
    <input type="number" v-model="size" />
  </p>
  <div :style="{ width: size + 'px', height: size + 'px', backgroundColor: color }"></div>
</template>

<script setup>
import { ref } from 'vue'

const color = ref('')
const size = ref(0)
</script>

<style scoped></style>
