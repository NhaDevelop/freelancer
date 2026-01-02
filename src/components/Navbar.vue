<template>
  <nav class="fixed top-0 left-0 right-0 z-50 glass-card border-b-2 border-white/20 shadow-2xl">
    <div class="container mx-auto px-6 py-5">
      <div class="flex items-center justify-between">
        <!-- Logo with gradient -->
        <div class="text-3xl font-black">
          <span class="bg-gradient-to-r from-cyan-400 via-purple-400 to-pink-400 bg-clip-text text-transparent animate-pulse">
            ✨ The Dev Quartet
          </span>
        </div>

        <!-- Desktop Navigation -->
        <div class="hidden md:flex items-center space-x-8">
          <a 
            v-for="link in navLinks" 
            :key="link.id"
            :href="link.href"
            class="text-gray-200 hover:text-cyan-400 transition-all duration-300 font-semibold text-lg relative group"
          >
            {{ link.label }}
            <span class="absolute bottom-0 left-0 w-0 h-0.5 bg-gradient-to-r from-cyan-400 to-purple-400 group-hover:w-full transition-all duration-300"></span>
          </a>
          <a href="#contact" class="btn-primary text-base px-6 py-2">
            📧 Contact Us
          </a>
        </div>

        <!-- Mobile Menu Button -->
        <button 
          @click="mobileMenuOpen = !mobileMenuOpen"
          class="md:hidden text-white focus:outline-none bg-gradient-to-r from-cyan-500 to-purple-500 p-3 rounded-lg hover:scale-110 transition-transform"
        >
          <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path 
              v-if="!mobileMenuOpen"
              stroke-linecap="round" 
              stroke-linejoin="round" 
              stroke-width="2" 
              d="M4 6h16M4 12h16M4 18h16"
            />
            <path 
              v-else
              stroke-linecap="round" 
              stroke-linejoin="round" 
              stroke-width="2" 
              d="M6 18L18 6M6 6l12 12"
            />
          </svg>
        </button>
      </div>

      <!-- Mobile Menu -->
      <div 
        v-if="mobileMenuOpen"
        class="md:hidden mt-6 pb-4 space-y-4"
      >
        <a 
          v-for="link in navLinks" 
          :key="link.id"
          :href="link.href"
          @click="mobileMenuOpen = false"
          class="block text-gray-200 hover:text-cyan-400 transition-colors duration-300 font-semibold text-lg py-2"
        >
          {{ link.label }}
        </a>
        <a 
          href="#contact" 
          @click="mobileMenuOpen = false"
          class="block btn-primary text-center"
        >
          📧 Contact Us
        </a>
      </div>
    </div>
  </nav>
</template>

<script setup>
import { ref } from 'vue'

const mobileMenuOpen = ref(false)

const navLinks = [
  { id: 1, label: '🏠 Home', href: '#home' },
  { id: 2, label: '👥 Team', href: '#team' },
  { id: 3, label: '🚀 Tech Stack', href: '#tech' },
  { id: 4, label: '⚡ Services', href: '#services' },
]
</script>
