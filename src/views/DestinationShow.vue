<template>
  <div>
    <h2>{{ destination.name }}</h2>
    <div class="destination-details">
      <img :src="`/images/${destination.image}`" :alt="destination.name" />
      <p>{{ destination.description }}</p>
    </div>
  </div>
</template>

<script setup>
import { computed } from 'vue'
import { useRoute } from 'vue-router'
import sourceData from '@/data.json'

const route = useRoute()

console.log(route.params.id)

const destinationId = computed(() => parseInt(route.params.id))
const destination = computed(() => {
  return sourceData.destinations.find((dest) => dest.id === destinationId.value)
})
</script>
