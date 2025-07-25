<template>
    <p>
       Price: <input v-model="price" type="number"></input>
    </p>
    <p>
        Quantity:<input v-model="quantity" type="number"></input>
    </p>
    <div>
        <p>
           Total Price: P{{ calculatePrice }}
        </p>
    </div>
</template>

<script setup>
import { ref, computed, reactive } from 'vue'
    const price = ref(0)
    const quantity = ref(0)
    const calculatePrice = computed(()=> price.value * quantity.value)
       
    
</script>

<style scoped></style>
