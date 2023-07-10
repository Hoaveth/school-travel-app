<script setup>
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <header>
    <div class="wrapper">
      <div id="nav">
        <RouterLink to="/">Home</RouterLink>
        <RouterLink to="/brazil">Brazil</RouterLink>
        <RouterLink to="/panama">Panama</RouterLink>
        <RouterLink to="/hawaii">Hawaii</RouterLink>
        <RouterLink to="/jamaica">Jamaica</RouterLink>
      </div>
    </div>
  </header>

  <div class="container">
    <RouterView />
  </div>
</template>
