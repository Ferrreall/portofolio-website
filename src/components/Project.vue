<script setup>
import { ref } from 'vue'

// Tinggal tambah/edit nama project kamu di array ini
const projects = ref([
  'Mobile Device Management (MDM) Web App',
  'Detective Maps (Crime Mapping & Analysis)',
  'Sistem Simulasi ATM (Logic & Transaction)',
  'ArcGIS JS API Mapping Integration',
  'Aplikasi Toko Peralatan Sekolah (CRUD & Inventory)',
])
</script>

<template>
  <section id="projects" class="py-16 px-6 max-w-3xl mx-auto">
    
    <!-- Section Header -->
    <div class="mb-8">
      <h2 class="text-xs uppercase font-semibold tracking-widest text-indigo-400 mb-1">
        Projects
      </h2>
      <h3 class="text-2xl font-bold text-zinc-100">
        Project yang Sudah Saya Kerjakan
      </h3>
    </div>

    <!-- Simple Project List -->
    <div class="border-t border-zinc-800 divide-y divide-zinc-800/60">
      <div 
        v-for="(project, index) in projects" 
        :key="index"
        class="py-4 flex items-center gap-4 group hover:pl-2 transition-all duration-200"
      >
        <!-- Bullet Indicator / Numbering -->
        <span class="text-xs font-mono text-indigo-400/70 group-hover:text-indigo-400">
          0{{ index + 1 }}
        </span>

        <!-- Project Title Text Only -->
        <p class="text-zinc-300 group-hover:text-zinc-100 font-medium text-sm sm:text-base">
          {{ project }}
        </p>
      </div>
    </div>

  </section>
</template>