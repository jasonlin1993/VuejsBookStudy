<script setup lang="ts">
import { ref, computed } from 'vue'

const price = ref<number>(100)
const quantity = ref<number>(10)
const subtotal = computed(() => {
  return price.value * quantity.value
})
</script>

<template>
  <div>
    <h1>單價: {{ price }}</h1>
    <h1>數量:{{ quantity }}</h1>
    <h1>總金額共{{ subtotal }}</h1>
  </div>
</template>
