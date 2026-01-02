<template>
  <section id="tech" class="py-24 relative overflow-hidden">
    <div class="container mx-auto px-6 relative z-10">
      <!-- Section Header -->
      <div class="text-center mb-20">
        <h2 class="text-5xl md:text-6xl font-black mb-6 bg-gradient-to-r from-cyan-400 via-purple-400 to-pink-400 bg-clip-text text-transparent flex items-center justify-center gap-4">
          <Rocket class="w-12 h-12 text-purple-400" :stroke-width="2.5" />
          Our Tech Stack
        </h2>
        <p class="text-gray-300 text-xl md:text-2xl max-w-3xl mx-auto font-medium">
          We leverage cutting-edge technologies to build robust, scalable, and beautiful applications
        </p>
      </div>

      <!-- Tech Categories -->
      <div class="space-y-16">
        <!-- Frontend -->
        <div>
          <h3 class="text-3xl md:text-4xl font-black mb-8 text-center bg-gradient-to-r from-cyan-400 to-blue-500 bg-clip-text text-transparent flex items-center justify-center gap-3">
            <Monitor class="w-10 h-10 text-cyan-400" />
            Frontend
          </h3>
          <div class="grid grid-cols-2 md:grid-cols-4 gap-6">
            <div 
              v-for="tech in techStack.frontend" 
              :key="tech.name"
              class="bg-white/10 backdrop-blur-lg border-2 border-white/20 rounded-2xl p-8 text-center hover:bg-white/20 hover:border-cyan-400/50 hover:shadow-2xl hover:shadow-cyan-500/30 hover:scale-110 transition-all duration-300"
            >
              <div class="w-20 h-20 mx-auto mb-4 flex items-center justify-center">
                <img :src="tech.logo" :alt="tech.name" class="w-full h-full object-contain" />
              </div>
              <div class="text-white font-bold text-xl">{{ tech.name }}</div>
            </div>
          </div>
        </div>

        <!-- Backend -->
        <div>
          <h3 class="text-3xl md:text-4xl font-black mb-8 text-center bg-gradient-to-r from-purple-400 to-pink-500 bg-clip-text text-transparent flex items-center justify-center gap-3">
            <Settings class="w-10 h-10 text-purple-400" />
            Backend
          </h3>
          <div class="grid grid-cols-2 md:grid-cols-4 gap-6">
            <div 
              v-for="tech in techStack.backend" 
              :key="tech.name"
              class="bg-white/10 backdrop-blur-lg border-2 border-white/20 rounded-2xl p-8 text-center hover:bg-white/20 hover:border-purple-400/50 hover:shadow-2xl hover:shadow-purple-500/30 hover:scale-110 transition-all duration-300"
            >
              <div class="w-20 h-20 mx-auto mb-4 flex items-center justify-center">
                <img :src="tech.logo" :alt="tech.name" class="w-full h-full object-contain" />
              </div>
              <div class="text-white font-bold text-xl">{{ tech.name }}</div>
            </div>
          </div>
        </div>

        <!-- Database & Mobile -->
        <div class="grid md:grid-cols-2 gap-12">
          <!-- Database -->
          <div>
            <h3 class="text-3xl md:text-4xl font-black mb-8 text-center bg-gradient-to-r from-green-400 to-emerald-500 bg-clip-text text-transparent flex items-center justify-center gap-3">
              <Database class="w-10 h-10 text-green-400" />
              Database
            </h3>
            <div class="grid grid-cols-1 gap-6">
              <div 
                v-for="tech in techStack.database" 
                :key="tech.name"
                class="bg-white/10 backdrop-blur-lg border-2 border-white/20 rounded-2xl p-10 text-center hover:bg-white/20 hover:border-green-400/50 hover:shadow-2xl hover:shadow-green-500/30 hover:scale-105 transition-all duration-300"
              >
                <div class="w-24 h-24 mx-auto mb-4 flex items-center justify-center">
                  <img :src="tech.logo" :alt="tech.name" class="w-full h-full object-contain" />
                </div>
                <div class="text-white font-bold text-2xl">{{ tech.name }}</div>
              </div>
            </div>
          </div>

          <!-- Mobile -->
          <div>
            <h3 class="text-3xl md:text-4xl font-black mb-8 text-center bg-gradient-to-r from-orange-400 to-red-500 bg-clip-text text-transparent flex items-center justify-center gap-3">
              <Smartphone class="w-10 h-10 text-orange-400" />
              Mobile
            </h3>
            <div class="grid grid-cols-2 gap-6">
              <div 
                v-for="tech in techStack.mobile" 
                :key="tech.name"
                class="bg-white/10 backdrop-blur-lg border-2 border-white/20 rounded-2xl p-8 text-center hover:bg-white/20 hover:border-orange-400/50 hover:shadow-2xl hover:shadow-orange-500/30 hover:scale-110 transition-all duration-300"
              >
                <div class="w-20 h-20 mx-auto mb-4 flex items-center justify-center">
                  <img :src="tech.logo" :alt="tech.name" class="w-full h-full object-contain" />
                </div>
                <div class="text-white font-bold text-xl">{{ tech.name }}</div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { Rocket, Monitor, Settings, Database, Smartphone } from 'lucide-vue-next'
import { techStack } from '../data/techStack'
</script>
