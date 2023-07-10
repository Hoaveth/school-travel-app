<script setup>
import sourceData from '@/data.json'
import { ref } from 'vue'
import { RouterLink } from 'vue-router'

let data = ref(sourceData)
</script>

<template>
  <div id="nav">
    <router-link class="logo" to="/"> Vue School Travel App</router-link>
    <router-link
      v-for="destination in data.destinations"
      :key="destination.id"
      :to="{ name: 'destination.show', params: { id: destination.id, slug: destination.slug } }"
    >
      {{ destination.name }}
    </router-link>
  </div>
</template>
