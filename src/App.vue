<template>
  <div class="container">
    <div class="card w-16 h-16 bg-blue-500">hehe</div>
  </div>
  
</template>

<script setup>
import { ref, computed, reactive, watch } from 'vue'

const movieList = reactive([
  { id: 1, title: 'Movie 1', year: 2000 },
  { id: 2, title: 'Movie 2', year: 2010 },
  { id: 3, title: 'Movie 3', year: 2020 },
])

let newMovie = reactive([{ id: 0, title: '', year: 0 }])
</script>

<style scoped></style>
