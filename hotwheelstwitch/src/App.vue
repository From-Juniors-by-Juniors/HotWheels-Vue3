<script setup>
import { ref, onMounted } from 'vue'
import { db } from './data/hotwheels'

const hotwheels = ref([])

onMounted(() => {
  hotwheels.value = db;
})
 
import Hotwheels from './components/HotWheels.vue'


</script>

<template>
  <Hotwheels 
  v-for="hotwheel in hotwheels"
  :hotwheel="hotwheel"
  />
</template>

<style scoped>
</style>
