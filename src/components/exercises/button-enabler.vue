<template>
  <form action="">
    <label for="email">Email:</label>
    <input v-model="email" type="text" id="email" /><br />
    <label for="passwrod">Password:</label>
    <input v-model="password" type="password" id="password" /><br />
    <input :disabled="!canSubmit" type="button" value="Submit" />
  </form>
</template>

<script setup>
import { ref, computed, reactive } from 'vue'
const email = ref('')
const password = ref('')

const canSubmit = computed(() => email.value !== '' && password.value !== '')
</script>

<style scoped></style>
