<script setup lang="ts">
import { ref } from 'vue';

const current = ref(0)

const updateFace = () => {
  current.value = Math.floor(Math.random() * 277)
}
</script>

<template>
  <main class="container">
    <h1>ASCII faces app</h1>
    <Faces :index="current" />
    <button @click="updateFace">Pick another one...</button>
  </main>
</template>

<style>
@import '@picocss/pico';
</style>
