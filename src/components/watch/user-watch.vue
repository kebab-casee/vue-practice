<template>
  <label for="age">Age: </label>
  <input v-model="user.age" type="text" id="age" />
</template>

<script setup>
import { ref, computed, reactive, watch } from 'vue'

const user = reactive({
  name: 'alice',
  age: 22,
})

watch(()=>user.age, (newval) => {
  console.log(`${user.name} is now ${newval} years old`)
})
</script>

<style scoped></style>
