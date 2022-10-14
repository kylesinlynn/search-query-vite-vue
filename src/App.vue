<script setup>
import { ref } from 'vue'
import Search from './components/Search.vue'
import Result from './components/Result.vue'

const query = ref('')

const testString = ref('Hello!')

</script>

<template>

  <Search @getQuery="(q) => query = q" />
  <Result :query="query" />

</template>

<style scoped>

</style>
