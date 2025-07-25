<template>
  <ul>
    <li v-for="task in completedTasks" :key="task.id">
      {{ task.name }}
    </li>
  </ul>
</template>

<script setup>
import { ref, computed, reactive } from 'vue'

const tasks = reactive([
  { id: 1, name: 'Wash dishes', done: true },
  { id: 2, name: 'Clean room', done: false },
  { id: 3, name: 'Do homework', done: true },
])

const completedTasks = computed(() => {
  return tasks.filter((task) => {
    return task.done
  })
})
</script>

<style scoped></style>
