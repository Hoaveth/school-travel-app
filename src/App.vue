<script setup>
import { RouterView, useRoute } from 'vue-router'
import TheNavigation from '@/components/TheNavigation.vue'

let route = useRoute()
</script>

<template>
  <header>
    <div class="wrapper">
      <TheNavigation />
    </div>
  </header>

  <div class="container">
    <RouterView :key="route.path" />
  </div>
</template>
