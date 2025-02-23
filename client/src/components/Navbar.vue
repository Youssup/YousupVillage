<script setup lang="ts">
import { ref, onMounted, onUnmounted } from 'vue'
const isHovered = ref(false)
const isAtTop = ref(true)
const isVisible = ref(true)

const handleScroll = () => {
  const atTop = window.scrollY < 10
  isAtTop.value = atTop
  
  // If we're at the top, always show the navbar
  if (atTop) {
    isVisible.value = true
  }
  // Only hide when not at top and not hovered
  else if (!isHovered.value) {
    isVisible.value = false
  }
}

const handleMouseEnter = () => {
  isHovered.value = true
  isVisible.value = true
}

const handleMouseLeave = () => {
  isHovered.value = false
  if (!isAtTop.value) {
    isVisible.value = false
  }
}

onMounted(() => {
  window.addEventListener('scroll', handleScroll)
})

onUnmounted(() => {
  window.removeEventListener('scroll', handleScroll)
})
</script>

<template>
  <nav 
    class="fixed top-0 w-full backdrop-blur-sm z-50 transition-all duration-300 ease-in-out"
    :class="[
      {'opacity-100': isVisible || isHovered},
      {'opacity-0': !isVisible && !isHovered},
      {'bg-white/80 shadow-sm': isHovered || isAtTop},
      {'bg-transparent': !isHovered && !isAtTop}
    ]"
    @mouseenter="handleMouseEnter"
    @mouseleave="handleMouseLeave"
  >
    <div class="max-w-7xl mx-auto px-4 py-4 flex justify-between items-center">
      <h1 class="text-3xl font-bold transition-opacity duration-300">Yoosup Song</h1>
      <div class="flex gap-6 py-4">
        <a href="#home" class="hover-grow transition-opacity duration-300 text-xl">Home</a>
        <!-- <a href="#experience" class="hover-grow transition-opacity duration-300 text-xl">Experience</a> -->
        <a href="#projects" class="hover-grow transition-opacity duration-300 text-xl">Projects</a>
      </div>
    </div>
  </nav>
</template>

<style scoped>
.hover-grow {
  transition: transform 0.2s ease-out;
}
.hover-grow:hover {
  transform: scale(1.05);
}
</style>