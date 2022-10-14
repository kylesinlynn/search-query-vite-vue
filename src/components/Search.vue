<script setup>

import { ref } from 'vue'

const query = ref('')

const emit = defineEmits(['getQuery'])

</script>

<template>

  <form @submit.prevent="emit('getQuery', query)">
    <input class="search-box" type="text" placeholder="Search" v-model="query">
    <button type="submit">🔍</button>
    <button type="reset">❌</button>
  </form>

</template>

<style scoped>
.search-box {
  width: 50em;
  padding: 1em 2em;
}
</style>