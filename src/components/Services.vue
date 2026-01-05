<template>
  <section id="services" class="py-24 bg-background relative">
    <div class="container mx-auto px-6">
      
      <!-- Services Header -->
      <div class="text-center mb-20">
        <span class="text-primary font-bold tracking-widest uppercase text-xs mb-4 block">What We Deliver</span>
        <h2 class="text-4xl md:text-5xl font-bold text-content mb-6 tracking-tight">
          Comprehensive Tech <span class="text-primary">Solutions</span>
        </h2>
        <p class="text-content-light max-w-2xl mx-auto text-lg leading-relaxed">
          We don't just write code; we engineer digital ecosystems tailored to your business goals.
        </p>
      </div>

      <!-- Services Grid -->
      <div class="grid md:grid-cols-3 gap-8 mb-32">
        <div 
          v-for="(service, index) in services" 
          :key="service.title"
          class="group bg-white border border-gray-100 rounded-2xl p-8 hover:border-cyan-400/50 hover:shadow-xl hover:shadow-cyan-400/20 transition-all duration-300 relative overflow-hidden"
        >
          <!-- Hover Accent - Cyan -->
          <div class="absolute top-0 left-0 w-1 h-0 bg-cyan-400 group-hover:h-full transition-all duration-300"></div>

          <div class="w-14 h-14 rounded-xl bg-cyan-50 flex items-center justify-center mb-8 group-hover:bg-cyan-400 group-hover:text-white transition-colors duration-300">
            <component :is="service.icon" class="w-7 h-7 text-cyan-500 group-hover:text-white transition-colors duration-300" />
          </div>
          
          <h3 class="text-2xl font-bold text-content mb-4 group-hover:text-cyan-600 transition-colors">
            {{ service.title }}
          </h3>
          
          <p class="text-content-light mb-8 leading-relaxed text-sm">
            {{ service.description }}
          </p>

          <ul class="space-y-3 pt-6 border-t border-gray-100">
            <li v-for="feature in service.features" :key="feature" class="flex items-center gap-3 text-content text-sm font-medium">
              <Check class="w-4 h-4 text-cyan-500 shrink-0" />
              <span>{{ feature }}</span>
            </li>
          </ul>
        </div>
      </div>

      <!-- Process Section -->
      <div id="process" class="bg-white rounded-3xl border border-gray-200 p-12 lg:p-16">
        <div class="text-center mb-16">
          <span class="text-primary font-bold tracking-widest uppercase text-xs mb-4 block">How We Work</span>
          <h3 class="text-3xl md:text-4xl font-bold text-content">Our Development Process</h3>
        </div>

        <div class="grid md:grid-cols-4 gap-8 relative">
          <!-- Connector Line (Desktop) -->
          <div class="hidden md:block absolute top-12 left-0 w-full h-0.5 bg-gray-100 -z-10"></div>

          <!-- Step 1 -->
          <div class="relative pt-4">
            <div class="w-16 h-16 rounded-full bg-white border-4 border-gray-100 flex items-center justify-center text-xl font-bold text-content mb-6 mx-auto relative z-10 shadow-sm">01</div>
            <h4 class="text-xl font-bold text-content text-center mb-4">Discovery</h4>
            <p class="text-sm text-content-light text-center leading-relaxed">
              We dive deep into your requirements, market, and goals to blueprint the perfect solution.
            </p>
          </div>

          <!-- Step 2 -->
          <div class="relative pt-4">
            <div class="w-16 h-16 rounded-full bg-white border-4 border-gray-100 flex items-center justify-center text-xl font-bold text-content mb-6 mx-auto relative z-10 shadow-sm">02</div>
            <h4 class="text-xl font-bold text-content text-center mb-4">Strategy</h4>
            <p class="text-sm text-content-light text-center leading-relaxed">
              Architecting the technical foundation and user experience design for scalability.
            </p>
          </div>

          <!-- Step 3 -->
          <div class="relative pt-4">
            <div class="w-16 h-16 rounded-full bg-white border-4 border-cyan-400 flex items-center justify-center text-xl font-bold text-cyan-500 mb-6 mx-auto relative z-10 shadow-lg shadow-cyan-400/30">03</div>
            <h4 class="text-xl font-bold text-content text-center mb-4">Development</h4>
            <p class="text-sm text-content-light text-center leading-relaxed">
              Agile sprints, code reviews, and rigorous testing to build robust, high-performance software.
            </p>
          </div>

          <!-- Step 4 -->
          <div class="relative pt-4">
            <div class="w-16 h-16 rounded-full bg-white border-4 border-gray-100 flex items-center justify-center text-xl font-bold text-content mb-6 mx-auto relative z-10 shadow-sm">04</div>
            <h4 class="text-xl font-bold text-content text-center mb-4">Launch</h4>
            <p class="text-sm text-content-light text-center leading-relaxed">
              Seamless deployment, ongoing support, and data-driven optimization.
            </p>
          </div>

        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { Zap, Check } from 'lucide-vue-next'
import { services } from '../data/services'
</script>
