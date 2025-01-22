<script setup lang="ts">
import { ref, computed } from 'vue'

const price = ref<number>(100)
const quantity = ref<number>(10)
const subtotal = computed(() => {
  return price.value * quantity.value
})

const arr = ref<string[]>(['008', 'JS', 'is', 'amazing'])
const book = ref<{ title: string; price: number; publishAt: string }>({
  title: 'Vue 3',
  price: 100,
  publishAt: '2019/9',
})

const lists = ref<Array<{ id: string; title: string; isDone: boolean }>>([
  { id: 'task001', title: '選項一', isDone: false },
  { id: 'task002', title: '選項二', isDone: false },
  { id: 'task003', title: '選項三', isDone: false },
])

const todoLists = computed(() => {
  return lists.value.filter((d) => !d.isDone)
})

const doneLists = computed(() => {
  return lists.value.filter((d) => d.isDone)
})
</script>

<template>
  <h1>Todo Lists</h1>
  <ul>
    <li v-for="i in todoLists" :key="i.id">
      <label>
        <input v-model="i.isDone" type="checkbox" />
        {{ i.title }}
      </label>
    </li>
  </ul>

  <h1>Done Lists</h1>
  <ul v-for="i in doneLists" :key="i.id">
    <label> <input type="checkbox" v-model="i.isDone" /> {{ i.title }}</label>
  </ul>
</template>
