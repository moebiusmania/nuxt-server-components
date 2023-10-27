<script setup lang="ts">
import { formatDistance } from 'date-fns'

const {
  label,
  date,
} = defineProps<{
  label: string
  date: string
}>()

const target = new Date(date)
const result = formatDistance(new Date(), target)
</script>

<template>
  <p>Days to {{ label }}: <strong>{{ result }}</strong></p>
</template>