<template>
  <div v-if="destination">
    <h2>{{ destination.name }}</h2>
    <div class="destination-details">
      <img :src="`/images/${destination.image}`" :alt="destination.name" />
      <p>{{ destination.description }}</p>
    </div>
  </div>
</template>

<script setup>
import { onBeforeMount, ref } from 'vue'
import { useRoute } from 'vue-router'

const route = useRoute()
let destination = ref(null)

onBeforeMount(() => {
  getDestination()
})

async function getDestination() {
  const response = await fetch(`https://travel-dummy-api.netlify.app/${route.params.slug}.json`)
  destination.value = await response.json()
}
</script>
