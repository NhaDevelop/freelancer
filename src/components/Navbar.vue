<template>
  <nav class="fixed top-0 left-0 right-0 z-50 bg-white/95 backdrop-blur-sm border-b border-border transition-all duration-300">
    <div class="container mx-auto px-6 h-20 flex items-center justify-between">
      <!-- Logo -->
      <a href="#" class="flex items-center gap-3 group">
        <div class="w-10 h-10 bg-primary/10 rounded-xl flex items-center justify-center group-hover:bg-primary transition-colors duration-300">
          <Layers class="w-6 h-6 text-primary group-hover:text-white transition-colors duration-300" />
        </div>
        <div class="flex flex-col">
          <span class="text-lg font-bold text-content leading-tight tracking-tight">The Dev Quartet</span>
          <span class="text-xs text-content-light font-medium tracking-wide uppercase">Tech Solutions</span>
        </div>
      </a>

      <!-- Desktop Navigation -->
      <div class="hidden md:flex items-center gap-8">
        <a 
          v-for="link in navLinks" 
          :key="link.id"
          :href="link.href"
          class="text-sm font-medium text-content hover:text-primary transition-colors duration-200"
        >
          {{ link.label }}
        </a>
      </div>

      <!-- CTA Button -->
      <div class="hidden md:flex items-center gap-4">
        <a href="#contact" class="px-6 py-2.5 rounded-lg bg-primary hover:bg-primary-hover text-white text-sm font-semibold shadow-lg shadow-primary/20 hover:shadow-primary/30 transform hover:-translate-y-0.5 transition-all duration-300">
          Get a Quote
        </a>
      </div>

      <!-- Mobile Menu Button -->
      <button 
        @click="mobileMenuOpen = !mobileMenuOpen"
        class="md:hidden text-content p-2 hover:bg-gray-100 rounded-lg transition-colors"
      >
        <Menu v-if="!mobileMenuOpen" class="w-6 h-6" />
        <X v-else class="w-6 h-6" />
      </button>
    </div>

    <!-- Mobile Menu -->
    <transition
      enter-active-class="transition duration-200 ease-out"
      enter-from-class="transform -translate-y-4 opacity-0"
      enter-to-class="transform translate-y-0 opacity-100"
      leave-active-class="transition duration-150 ease-in"
      leave-from-class="transform translate-y-0 opacity-100"
      leave-to-class="transform -translate-y-4 opacity-0"
    >
      <div 
        v-if="mobileMenuOpen"
        class="md:hidden border-t border-border bg-white"
      >
        <div class="container mx-auto px-6 py-6 space-y-4">
          <a 
            v-for="link in navLinks" 
            :key="link.id"
            :href="link.href"
            @click="mobileMenuOpen = false"
            class="block text-base font-medium text-content hover:text-primary transition-colors"
          >
            {{ link.label }}
          </a>
          <hr class="border-border" />
          <a 
            href="#contact" 
            @click="mobileMenuOpen = false"
            class="block w-full py-3 text-center rounded-lg bg-primary text-white font-semibold shadow-md active:scale-95 transition-transform"
          >
            Get a Quote
          </a>
        </div>
      </div>
    </transition>
  </nav>
</template>

<script setup>
import { ref } from 'vue'
import { Layers, Menu, X } from 'lucide-vue-next'

const mobileMenuOpen = ref(false)

const navLinks = [
  { id: 1, label: 'Work', href: '#tech' },
  { id: 2, label: 'Services', href: '#services' },
  { id: 3, label: 'Process', href: '#process' }, // New section
  { id: 4, label: 'Team', href: '#team' },
]
</script>
