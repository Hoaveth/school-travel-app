<script setup>
import sourceData from '@/data.json'
import { ref } from 'vue'
import { RouterLink } from 'vue-router'

let data = ref(sourceData)
</script>

<template>
  <div class="home">
    <h1>All Destinations</h1>
    <div class="destinations">
      <RouterLink
        v-for="destination in data.destinations"
        :key="destination.id"
        :to="`/${destination.slug}`"
        class="link"
      >
        <h2>{{ destination.name }}</h2>
        <img :src="`/images/${destination.image}`" :alt="destination.name" />
      </RouterLink>
    </div>
  </div>
</template>

<style>
.link {
  padding: 10px;
}
</style>
