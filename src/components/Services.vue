<template>
  <section id="services" class="py-24 relative overflow-hidden">
    <div class="container mx-auto px-6 relative z-10">
      <!-- Section Header -->
      <div class="text-center mb-20">
        <h2 class="text-5xl md:text-6xl font-black mb-6 bg-gradient-to-r from-cyan-400 via-purple-400 to-pink-400 bg-clip-text text-transparent flex items-center justify-center gap-4">
          <Zap class="w-12 h-12 text-purple-400" :stroke-width="2.5" />
          Our Services
        </h2>
        <p class="text-gray-300 text-xl md:text-2xl max-w-3xl mx-auto font-medium">
          From concept to deployment, we offer comprehensive development services tailored to your needs
        </p>
      </div>

      <!-- Services Grid -->
      <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
        <div 
          v-for="(service, index) in services" 
          :key="service.id"
          class="bg-white/10 backdrop-blur-lg border-2 border-white/20 rounded-2xl p-10 hover:bg-white/20 hover:border-cyan-400/50 hover:shadow-2xl hover:shadow-cyan-500/30 hover:-translate-y-2 transition-all duration-300"
        >
          <!-- Icon -->
          <div class="w-20 h-20 mx-auto mb-6 rounded-2xl bg-gradient-to-br flex items-center justify-center"
            :class="getIconGradient(index)">
            <component :is="getServiceIcon(index)" class="w-12 h-12 text-white" :stroke-width="2" />
          </div>

          <!-- Title -->
          <h3 class="text-3xl font-black mb-5 bg-gradient-to-r from-cyan-400 to-purple-500 bg-clip-text text-transparent">
            {{ service.title }}
          </h3>

          <!-- Description -->
          <p class="text-gray-300 mb-8 text-lg leading-relaxed">
            {{ service.description }}
          </p>

          <!-- Technologies -->
          <div class="mb-8">
            <h4 class="text-sm font-bold text-cyan-400 mb-4 uppercase flex items-center gap-2">
              <Code class="w-4 h-4" />
              Technologies:
            </h4>
            <div class="flex flex-wrap gap-3">
              <span 
                v-for="tech in service.technologies" 
                :key="tech"
                class="px-4 py-2 rounded-full text-sm font-semibold bg-white/10 border border-white/20 text-white hover:bg-white/20 transition-all"
              >
                {{ tech }}
              </span>
            </div>
          </div>

          <!-- Features -->
          <div>
            <h4 class="text-sm font-bold text-purple-400 mb-4 uppercase flex items-center gap-2">
              <Sparkles class="w-4 h-4" />
              Key Features:
            </h4>
            <ul class="space-y-3">
              <li 
                v-for="feature in service.features" 
                :key="feature"
                class="text-base text-gray-300 flex items-start"
              >
                <Check class="w-5 h-5 text-cyan-400 mr-3 flex-shrink-0 mt-0.5" :stroke-width="3" />
                <span>{{ feature }}</span>
              </li>
            </ul>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { Zap, Code, Sparkles, Check, Gem, Building2, Smartphone } from 'lucide-vue-next'
import { services } from '../data/services'

const getServiceIcon = (index) => {
  const icons = [Gem, Building2, Smartphone]
  return icons[index % icons.length]
}

const getIconGradient = (index) => {
  const gradients = [
    'from-cyan-500 to-blue-500',
    'from-purple-500 to-pink-500',
    'from-green-500 to-emerald-500'
  ]
  return gradients[index % gradients.length]
}

console.log('Services count:', services.length)
console.log('Services data:', services)
</script>
