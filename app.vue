<script setup lang="ts">
import { ref } from 'vue';

const list = [
  { label: "Halloween", date: "10-31-2023" },
  { label: "NYE", date: "01-01-2024" },
]

const current = ref(0)
const buttonLabel = current.value === 0 ? list[1].label : list[0].label

const switchDate = () => {
  current.value = current.value === 0 ? 1 : 0
}
</script>

<template>
  <div>
    <h1>Date countdown app</h1>
    <Countdown :label="list[current].label" :date="list[current].date" />
    <button @click="switchDate">Switch to {{ buttonLabel }} </button>
  </div>
</template>
