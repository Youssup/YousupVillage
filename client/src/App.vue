<script setup lang="ts">
import { RouterView } from 'vue-router'
import Navbar from './components/Navbar.vue'
</script>

<template>
  <header>
    <nav>
      <Navbar />
    </nav>
  </header>
  <div>
    <RouterView />
  </div>
</template>

<style scoped>
</style>
