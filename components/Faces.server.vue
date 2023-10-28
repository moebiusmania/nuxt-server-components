<script setup lang="ts">
import ascii from 'ascii-faces'

const {
  index = 0
} = defineProps<{
  index: number
}>()

</script>

<template>
  <p>Here is some cool ASCII face!</p>
  <pre><code>{{ ascii.faces[index] }}</code></pre>
</template>