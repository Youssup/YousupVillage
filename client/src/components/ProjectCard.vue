<template>
    <div class="bg-white rounded-3xl p-6 shadow-lg hover-lift group">
      <div class="relative overflow-hidden rounded-xl mb-4">
        <img 
          :src="project.imageUrl" 
          :alt="project.title" 
          class="h-96 object-cover" 
        />
        <div class="absolute inset-0 bg-black/70 opacity-0 hover:opacity-100 transition-opacity duration-300 flex items-center justify-center">
          <div class="text-white text-center p-6">
            <h4 class="text-xl font-bold mb-4">Key Features</h4>
            <ul class="text-sm space-y-2">
              <li v-for="feature in project.features" :key="feature" class="flex items-center">
                <span class="mr-2">•</span>{{ feature }}
              </li>
            </ul>
          </div>
        </div>
      </div>
      <div class="space-y-6">
        <div>
          <h3 class="text-2xl font-bold text-gray-600">{{ project.title }}</h3>
          <p class="text-neutral-500 mt-3">{{ project.description }}</p>
        </div>
        <div class="space-y-4">
          <h4 class="font-semibold">Technologies Used:</h4>
          <div class="flex flex-wrap gap-2">
            <span 
              v-for="tech in project.technologies" 
              :key="tech.name"
              class="px-3 py-1 rounded-full text-sm"
              :class="tech.class"
            >
              {{ tech.name }}
            </span>
          </div>
        </div>
      </div>
    </div>
  </template>
  
  <script setup lang="ts">
  defineProps({
    project: {
      type: Object,
      required: true
    }
  });
  </script>
  
  <style scoped>
  .hover-lift {
    transition: transform 0.2s ease-in-out;
  }
  
  .hover-lift:hover {
    transform: translateY(-4px);
  }
  </style>