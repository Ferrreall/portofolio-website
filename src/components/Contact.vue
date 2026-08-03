<script setup>
import { ref } from 'vue'

// Sesuaikan email dan link medsos/github kamu di sini
const email = ref('ferramdanii@gmail.com')
const socialLinks = ref([
  { name: 'GitHub', url: 'https://github.com/Ferrreall' },
  { name: 'Instagram', url: 'https://instagram.com/fwrrrdn' }
])
</script>

<template>
  <section id="contact" class="py-20 px-6 max-w-3xl mx-auto text-left">
    
    <!-- Section Header -->
    <div class="mb-8">
      <h2 class="text-xs uppercase font-semibold tracking-widest text-indigo-400 mb-1">
        Contact
      </h2>
      <h3 class="text-2xl sm:text-3xl font-bold text-zinc-100">
        Mari Bekerja Sama / Berdiskusi
      </h3>
    </div>

    <!-- Description -->
    <p class="text-zinc-400 text-sm sm:text-base leading-relaxed mb-8 max-w-xl">
      Tertarik untuk merekrut, mengajak berkolaborasi dalam project, atau sekadar bertanya-tanya? Jangan ragu buat sapa saya lewat email atau media sosial di bawah ini!
    </p>

    <!-- Email Action Box -->
    <div class="p-6 rounded-xl bg-zinc-900 border border-zinc-800/80 mb-10 flex flex-col sm:flex-row items-start sm:items-center justify-between gap-4">
      <div>
        <p class="text-xs font-mono text-zinc-500 uppercase tracking-wider mb-1">Direct Email</p>
        <p class="text-zinc-200 font-medium font-mono text-sm sm:text-base">{{ email }}</p>
      </div>

      <a 
        :href="`https://mail.google.com/mail/?view=cm&fs=1&to=${email}`" 
        target="_blank"
        rel="noopener noreferrer"
        class="px-5 py-2.5 rounded-lg bg-indigo-600 hover:bg-indigo-500 text-white font-medium text-xs sm:text-sm transition-colors duration-200"
      >
        Send Email
      </a>
    </div>

    <!-- Social Links & Footer -->
    <div class="pt-8 border-t border-zinc-800/60 flex flex-col sm:flex-row items-center justify-between gap-4 text-xs text-zinc-500">
      
      <!-- Social Media List -->
      <div class="flex items-center gap-4">
        <a 
          v-for="(link, index) in socialLinks" 
          :key="index"
          :href="link.url"
          target="_blank"
          rel="noopener noreferrer"
          class="hover:text-indigo-400 transition-colors duration-200 font-mono"
        >
          {{ link.name }}
        </a>
      </div>

      <!-- Copyright -->
      <p class="font-mono text-zinc-600">
        © {{ new Date().getFullYear() }} — Built with Vue 3 & Tailwind CSS
      </p>

    </div>

  </section>
</template>