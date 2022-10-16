<script setup lang="ts">
import ProgressBar from "./components/ProgressBar.vue";
</script>

<template>
  <main>
    <progress-bar :done="20" />
    <progress-bar :done="50" :reverse="true" />
    <progress-bar :done="75" :reverse="true" />
  </main>
</template>

<style scoped></style>
