<template>
    <div class="bg-white rounded-3xl p-6 shadow-lg hover-lift group">
      <!-- Company Logo and Info Section -->
      <div class="relative overflow-hidden rounded-xl mb-6">
        <div class="relative h-40 bg-gray-50 flex items-center justify-center p-6">
          <img
            v-if="experience.logoUrl"
            :src="experience.logoUrl"
            :alt="`${experience.company} logo`"
            class="max-h-28 max-w-full object-contain transition-transform duration-300 group-hover:scale-105"
          />
          <div v-else class="w-full h-full flex items-center justify-center">
            <h3 class="text-3xl font-bold text-gray-400">{{ experience.company }}</h3>
          </div>
          
          <!-- Hover overlay with achievements -->
          <a
            v-if="experience.companyUrl"
            :href="experience.companyUrl"
            target="_blank"
            rel="noopener noreferrer"
            class="absolute inset-0"
          >
            <div class="absolute inset-0 bg-black/70 opacity-0 hover:opacity-100 transition-opacity duration-300 flex items-center justify-center">
              <div class="text-white text-center p-6">
                <h4 class="text-xl font-bold mb-4">Key Achievements</h4>
                <ul class="text-sm space-y-2">
                  <li v-for="(achievement, i) in experience.achievements" :key="i" class="flex items-center">
                    <span class="mr-2">•</span>{{ achievement.text }}
                  </li>
                </ul>
              </div>
            </div>
          </a>
        </div>
      </div>
      
      <div class="space-y-6">
        <!-- Title and Description -->
        <div>
          <div class="flex justify-between items-start">
            <h3 class="text-2xl font-bold text-gray-600">{{ experience.role }}</h3>
            <span class="text-sm text-gray-500 whitespace-nowrap">
              {{ experience.startDate }} — {{ experience.endDate || 'Present' }}
            </span>
          </div>
          <p class="text-lg text-gray-600 mt-1">{{ experience.company }}</p>
          <p v-if="experience.location" class="text-sm text-neutral-500 mt-1">{{ experience.location }}</p>
          <p class="text-neutral-500 mt-3">{{ experience.description }}</p>
        </div>
        
        <!-- Skills Section -->
        <div class="space-y-4">
          <h4 class="font-semibold">Skills & Technologies:</h4>
          <div class="flex flex-wrap gap-2">
            <template v-for="skill in experience.skills" :key="skill.name">
              <!-- Badge with URL if available -->
              <a
                v-if="skill.badgeUrl && skill.url"
                :href="skill.url"
                target="_blank"
                rel="noopener noreferrer"
              >
                <img
                  :src="skill.badgeUrl"
                  :alt="skill.name"
                  class="h-6"
                />
              </a>
              <!-- Badge without URL -->
              <img
                v-else-if="skill.badgeUrl"
                :src="skill.badgeUrl"
                :alt="skill.name"
                class="h-6"
              />
              <!-- Text fallback -->
              <span
                v-else
                class="px-3 py-1 bg-gray-100 text-gray-600 text-xs font-medium rounded-full"
              >
                {{ skill.name }}
              </span>
            </template>
          </div>
        </div>
      </div>
    </div>
  </template>
  
  <script setup lang="ts">
  interface Skill {
    name: string;
    badgeUrl?: string;
    url?: string;
  }
  
  interface Achievement {
    text: string;
  }
  
  interface Experience {
    company: string;
    role: string;
    logoUrl: string;
    startDate: string;
    endDate?: string;
    location?: string;
    description: string;
    skills: Skill[];
    achievements: Achievement[];
    companyUrl?: string;
  }
  
  defineProps<{
    experience: Experience;
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