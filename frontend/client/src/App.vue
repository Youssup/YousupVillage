<script setup lang="ts">
import { RouterView } from 'vue-router'
import Navbar from './components/Navbar.vue'
import Footer from './components/Footer.vue'
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
  <div class="footer">
    <Footer />
  </div>
</template>

<style scoped>
.footer {
  position: fixed;
  bottom: 1px;
  width: 100%;
  transform: translateY(80%);
  transition: transform 0.5s;
  justify-content: center;
}

.footer:hover {
  transform: translateY(0);
}
</style>
