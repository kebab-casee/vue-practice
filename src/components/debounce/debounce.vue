<template>
  <div class="p-4">
    <h2 class="text-lg font-bold mb-2">Vue Debounce Demo</h2>
    <input
      v-model="searchQuery"
      type="text"
      placeholder="Type to search..."
      class="border p-2 rounded w-full mb-4"
    />
    <p>Search Query: {{ searchQuery }}</p>
    <p class="text-green-600 font-semibold mt-2">Debounced Query: {{ debouncedQuery }}</p>
  </div>
</template>

<script setup>
import { ref, watch } from 'vue'

// Reactive search input
const searchQuery = ref('')

// Debounced value to display
const debouncedQuery = ref('')

// Timeout reference for debounce
let timeoutId

watch(searchQuery, (newValue) => {
  // Clear previous timeout on every input change
  clearTimeout(timeoutId)

  // Set a new timeout to update debouncedQuery after 500ms of inactivity
  timeoutId = setTimeout(() => {
    debouncedQuery.value = newValue
    console.log('Debounced Value:', newValue)
    // You could place your API call here
  }, 500)
})
</script>

<style scoped>
body {
  font-family: 'Arial';
}
</style>
