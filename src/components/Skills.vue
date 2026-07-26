<script setup>
import { ref } from 'vue'

const skillCategories = ref([
  {
    category: 'Full-Stack & Languages',
    skills: [
      { name: 'PHP', icon: 'https://cdn.simpleicons.org/php/777BB4' },
      { name: 'JavaScript', icon: 'https://cdn.simpleicons.org/javascript/F7DF1E' },
      { name: 'HTML5 & CSS', icon: 'https://cdn.simpleicons.org/html5/E34F26' },
      { name: 'SQL', icon: 'https://cdn.simpleicons.org/sqlite/003B57' }
    ]
  },
  {
    category: 'Frameworks & Libraries',
    skills: [
      { name: 'Laravel', icon: 'https://cdn.simpleicons.org/laravel/FF2D20' },
      { name: 'Vue.js', icon: 'https://cdn.simpleicons.org/vuedotjs/4FC08D' },
      { name: 'Tailwind CSS', icon: 'https://cdn.simpleicons.org/tailwindcss/06B6D4' },
      { name: 'ArcGIS JS API', icon: 'https://cdn.simpleicons.org/arcgis/007AC2' }
    ]
  },
  {
    category: 'Tools, DB & Workflow',
    skills: [
      { name: 'Git & GitHub', icon: 'https://cdn.simpleicons.org/git/F05032' },
      { name: 'MySQL', icon: 'https://cdn.simpleicons.org/mysql/4479A1' },
      { name: 'PostgreSQL', icon: 'https://cdn.simpleicons.org/postgresql/4169E1' },
      { name: 'Navicat', icon: 'https://cdn.simpleicons.org/datagrip/000000' },
      { name: 'Vite', icon: 'https://cdn.simpleicons.org/vite/646CFF' },
      { name: 'Laragon', icon: 'https://cdn.simpleicons.org/serverless/FD5750' },
      { name: 'Postman', icon: 'https://cdn.simpleicons.org/postman/FF6C37' }
    ]
  }
])
</script>

<template>
  <section id="skills" class="py-16 px-6 max-w-3xl mx-auto">
    
    <!-- Section Header -->
    <div class="mb-10 text-left">
      <h2 class="text-xs uppercase font-semibold tracking-widest text-indigo-400 mb-1">
        Skills
      </h2>
      <h3 class="text-2xl font-bold text-zinc-100">
        Tech Stack & Tooling
      </h3>
    </div>

    <!-- Skills Category List -->
    <div class="space-y-8 text-left">
      <div 
        v-for="(cat, index) in skillCategories" 
        :key="index"
        class="border-b border-zinc-800/80 pb-6 last:border-none"
      >
        <h4 class="text-sm font-semibold text-zinc-400 mb-3 tracking-wide">
          {{ cat.category }}
        </h4>

        <div class="flex flex-wrap gap-2">
          <span 
            v-for="(skill, sIndex) in cat.skills" 
            :key="sIndex"
            class="inline-flex items-center gap-2 px-3 py-1.5 rounded-md bg-zinc-900 border border-zinc-800 text-zinc-300 text-xs sm:text-sm font-mono hover:border-indigo-500/40 hover:text-indigo-300 transition-colors duration-200"
          >
            <!-- Mini Icon SVG dari CDN -->
            <img 
              :src="skill.icon" 
              :alt="skill.name" 
              class="w-3.5 h-3.5 object-contain"
            />
            <span>{{ skill.name }}</span>
          </span>
        </div>
      </div>
    </div>

  </section>
</template>