<template>
  <section id="tech" class="py-20 bg-white">
    <div class="container mx-auto px-6">
      <div class="text-center mb-20">
        <span class="text-primary font-bold tracking-widest uppercase text-xs mb-4 block">Our Arsenal</span>
        <h2 class="text-3xl md:text-4xl font-bold text-content mb-6">
          Technology <span class="text-primary">Stack</span>
        </h2>
        <p class="text-content-light max-w-2xl mx-auto text-lg leading-relaxed">
          We use industry-standard, scalable technologies to build future-proof software.
        </p>
      </div>

      <div class="space-y-16">
        <!-- Frontend -->
        <div class="space-y-6">
          <h3 class="text-xl font-bold mb-6 flex items-center gap-3 text-content border-b border-gray-200 pb-3">
            <Monitor class="w-5 h-5 text-primary" />
            Frontend & Mobile
          </h3>
          <div class="grid grid-cols-2 md:grid-cols-4 lg:grid-cols-5 gap-4">
             <div 
              v-for="tech in [...techStack.frontend, ...techStack.mobile]" 
              :key="tech.name"
              class="group bg-white border border-gray-200 rounded-lg p-4 flex items-center gap-4 transition-all duration-300 hover:border-primary/50 hover:shadow-md hover:-translate-y-0.5"
            >
              <img :src="tech.logo" :alt="tech.name" class="w-8 h-8 object-contain group-hover:scale-110 transition-transform duration-300" />
              <span class="font-medium text-sm text-content group-hover:text-primary transition-colors">{{ tech.name }}</span>
            </div>
          </div>
        </div>

        <!-- Backend & Infrastructure -->
        <div class="space-y-6">
          <h3 class="text-xl font-bold mb-6 flex items-center gap-3 text-content border-b border-gray-200 pb-3">
            <Settings class="w-5 h-5 text-primary" />
            Backend & Infrastructure
          </h3>
          <div class="grid grid-cols-2 md:grid-cols-4 lg:grid-cols-5 gap-4">
             <div 
              v-for="tech in [...techStack.backend, ...techStack.devops]" 
              :key="tech.name"
              class="group bg-white border border-gray-200 rounded-lg p-4 flex items-center gap-4 transition-all duration-300 hover:border-primary/50 hover:shadow-md hover:-translate-y-0.5"
            >
              <img :src="tech.logo" :alt="tech.name" class="w-8 h-8 object-contain group-hover:scale-110 transition-transform duration-300" />
              <span class="font-medium text-sm text-content group-hover:text-primary transition-colors">{{ tech.name }}</span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { Layers, Monitor, Settings, Database, Smartphone } from 'lucide-vue-next'
import { techStack } from '../data/techStack'
</script>
