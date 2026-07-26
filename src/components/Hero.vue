<template>
  <section id="hero" class=" flex items-center justify-center pt-20 pb-16 px-6">
    <div class="max-w-4xl mx-auto text-center space-y-8">
      
      <!-- Status Badge -->
      <div class="inline-flex items-center gap-2 px-3.5 py-1.5 rounded-full bg-indigo-500/10 border border-indigo-500/20 text-indigo-400 text-xs sm:text-sm font-medium">
        <span class="w-2 h-2 rounded-full bg-indigo-400 animate-pulse"></span>
        <span>Available for Projects & Internship</span>
      </div>

      <!-- Main Headline -->
      <h1 class="text-4xl sm:text-6xl font-extrabold text-zinc-100 tracking-tight leading-tight sm:leading-tight">
        Building modern web apps with <br class="hidden sm:inline" />
        <span class="text-transparent bg-clip-text bg-linear-to-r from-indigo-400 to-indigo-200">
          clean code & great UX.
        </span>
      </h1>

      <!-- Short Bio / Description -->
      <p class="max-w-2xl mx-auto text-zinc-400 text-base sm:text-lg leading-relaxed">
        Halo, saya <span class="text-zinc-200 font-medium">Feri Ramdani</span>. Full-Stack Web Developer berbasis di Indonesia. Suka merancang aplikasi web dari fondasi backend hingga tampilan frontend yang bersih dan rapi.
      </p>

      <!-- Action Buttons -->
      <div class="flex flex-col sm:flex-row items-center justify-center gap-4 pt-4">
        <a 
          href="#projects" 
          class="w-full sm:w-auto px-6 py-3 rounded-lg bg-indigo-600 hover:bg-indigo-500 text-white font-medium text-sm transition-colors duration-200 shadow-lg shadow-indigo-600/20"
        >
          View My Work
        </a>
        <a 
          href="#contact" 
          class="w-full sm:w-auto px-6 py-3 rounded-lg bg-zinc-900 hover:bg-zinc-800 text-zinc-300 border border-zinc-800 font-medium text-sm transition-colors duration-200"
        >
          Get in Touch
        </a>
      </div>

    </div>
  </section>
</template>