<script setup>
import { RouterView } from 'vue-router'
import TheNavigation from '@/components/TheNavigation.vue'
</script>

<template>
  <header>
    <div class="wrapper">
      <TheNavigation />
    </div>
  </header>

  <div class="container">
    <RouterView />
  </div>
</template>
