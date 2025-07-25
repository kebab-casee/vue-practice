<template>
  <label for="search">Search: </label>
  <input v-model="searchQuery" type="text" id="search" />
  <p>
    {{ searchQuery }}
  </p>
</template>

<script setup>
import { ref, computed, reactive, watch } from 'vue'
const searchQuery = ref('')

watch(searchQuery, (newVal) => {
  console.log(`Searching for ${newVal}`)
})
</script>

<style scoped></style>
