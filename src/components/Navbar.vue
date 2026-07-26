<script setup>
import { ref, onMounted, onUnmounted } from 'vue'

const activeSection = ref('hero')

const navItems = [
  { name: 'About', href: '#hero', id: 'hero' },
  { name: 'Projects', href: '#projects', id: 'projects' },
  { name: 'Skills', href: '#skills', id: 'skills' },
  { name: 'Contact', href: '#contact', id: 'contact' },
]

let observer = null

onMounted(() => {
  // IntersectionObserver untuk melacak section mana yang sedang dilihat
  const options = {
    root: null,
    rootMargin: '-20% 0px -60% 0px', // Trigger saat section berada di area pandang atas-tengah
    threshold: 0
  }

  observer = new IntersectionObserver((entries) => {
    entries.forEach((entry) => {
      if (entry.isIntersecting) {
        activeSection.value = entry.target.id
      }
    })
  }, options)

  // Ambil semua section berdasarkan ID
  navItems.forEach((item) => {
    const el = document.getElementById(item.id)
    if (el) observer.observe(el)
  })
})

onUnmounted(() => {
  if (observer) observer.disconnect()
})
</script>

<template>
  <nav class="fixed top-0 left-0 w-full z-50 bg-zinc-950/80 backdrop-blur-md border-b border-zinc-800/50">
    <div class="max-w-5xl mx-auto px-6 h-16 flex items-center justify-between">
      
      <!-- Kiri Atas: Branding (Ganti tulisan Portofolio) -->
      <a href="#hero" class="text-base font-bold tracking-tight text-zinc-100 hover:text-indigo-400 transition-colors">
        Feroo<span class="text-indigo-400">.dev</span>
      </a>

      <!-- Menu Navigasi Tengah -->
      <div class="hidden md:flex items-center space-x-8 text-sm font-medium">
        <a 
          v-for="item in navItems" 
          :key="item.id"
          :href="item.href"
          :class="[
            'relative py-1 transition-colors duration-200',
            activeSection === item.id ? 'text-indigo-400 font-semibold' : 'text-zinc-400 hover:text-zinc-200'
          ]"
        >
          {{ item.name }}
          <!-- Indicator Garis Bawah Aktif -->
          <span 
            v-if="activeSection === item.id" 
            class="absolute bottom-0 left-0 w-full h-0.5 bg-indigo-400 rounded-full transition-all duration-300"
          ></span>
        </a>
      </div>

      <!-- Kanan Atas: Link GitHub Direct -->
      <a 
        href="https://github.com/Ferrreall" 
        target="_blank"
        rel="noopener noreferrer"
        class="px-3.5 py-1.5 rounded-lg bg-zinc-900 hover:bg-zinc-800 text-zinc-300 hover:text-white border border-zinc-800 text-xs font-mono font-medium transition-all duration-200 flex items-center gap-2"
      >
        <span>GitHub</span>
        <!-- Arrow Icon Kecil -->
        <span class="text-zinc-500 text-xs">↗</span>
      </a>

    </div>
  </nav>
</template>