<template>
  <div class="bg-white rounded-3xl p-6 shadow-lg hover-lift group">
    <div class="relative overflow-hidden rounded-xl mb-4">
      <!-- Image links to GitHub only if URL exists -->
      <div class="relative">
        <img
          :src="project.imageUrl"
          :alt="project.title"
          class="h-96 w-full object-cover transition-transform duration-300"
          :class="{ 'hover:scale-105': project.githubUrl }"
        />
        <a 
          v-if="project.githubUrl"
          :href="project.githubUrl" 
          target="_blank" 
          rel="noopener noreferrer"
          class="absolute inset-0"
        >
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
        </a>
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
          <a
            v-for="tech in project.technologies"
            :key="tech.name"
            :href="tech.url"
            target="_blank"
            rel="noopener noreferrer"
          >
            <img
              :src="tech.badgeUrl"
              :alt="tech.name"
              class="h-6"
            />
          </a>
        </div>
      </div>
      <!-- Buttons container - only shown if at least one URL exists -->
      <div v-if="project.githubUrl || project.demoUrl" class="flex gap-4 pt-4">
        <a
          v-if="project.demoUrl"
          :href="project.demoUrl"
          target="_blank"
          rel="noopener noreferrer"
          class="flex-1 bg-blue-600 text-white px-6 py-2 rounded-lg font-medium text-center hover:bg-blue-700 transition-colors duration-200"
        >
          Live Demo
        </a>
        <a
          v-if="project.githubUrl"
          :href="project.githubUrl"
          target="_blank"
          rel="noopener noreferrer"
          class="flex-1 bg-gray-800 text-white px-6 py-2 rounded-lg font-medium text-center hover:bg-gray-900 transition-colors duration-200"
        >
          GitHub
        </a>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
interface Technology {
  name: string;
  badgeUrl: string;
  url: string;
}

interface Project {
  imageUrl: string;
  githubUrl?: string;  // Made optional with '?'
  demoUrl?: string;    // Made optional with '?'
  title: string;
  description: string;
  features: string[];
  technologies: Technology[];
}

defineProps<{
  project: Project;
}>();
</script>

<style scoped>
.hover-lift {
  transition: transform 0.2s ease-in-out;
}
.hover-lift:hover {
  transform: translateY(-4px);
}
</style>