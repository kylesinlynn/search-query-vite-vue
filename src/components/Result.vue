<script setup>
import { computed } from "vue";
import titles from '../data.json'

const props = defineProps({
  query: String
})

const filteredTitles = computed(() => titles.filter(s => s.Name.toLowerCase().includes(props.query.toLowerCase())))

</script>

<template>

  <h2>Results:</h2>
  <div>
    <div v-if="filteredTitles.length">
      <div v-for="title in filteredTitles" :key="title.Page">
        <p>{{ title.Name }}<a href="{{ title.Page }}" >🏹</a></p>
      </div>
    </div>
    <p v-else>No result.</p>
  </div>

</template>

<style scoped>

</style>