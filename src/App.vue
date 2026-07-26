<script setup>
import Navbar from './components/Navbar.vue'
import Hero from './components/Hero.vue'
import Project from './components/Project.vue'
import Skills from './components/Skills.vue'
import Contact from './components/Contact.vue'
</script>

<template>
  <div class="min-h-screen bg-zinc-950  text-slate-100 font-sans">
    <Navbar />
    <main class="pt-24 text-center">
      <Hero />
      <Project />
      <Skills />
      <Contact />
    </main>
  </div>
</template>

<style scoped></style>
