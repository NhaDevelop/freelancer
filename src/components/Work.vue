<template>
  <section id="work" class="py-20 bg-background relative">
    <div class="container mx-auto px-6">
      <div class="text-center mb-16">
        <span class="text-primary font-bold tracking-widest uppercase text-xs mb-4 block">Our Portfolio</span>
        <h2 class="text-3xl md:text-4xl font-bold text-content mb-6">
          Selected <span class="text-primary">Work</span>
        </h2>
        <p class="text-content-light max-w-2xl mx-auto text-lg leading-relaxed">
          Delivering high-impact digital solutions for ambitious brands.
        </p>
      </div>

      <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-8">
        <!-- Project 1: IRIP -->
        <div
          class="group bg-white rounded-2xl overflow-hidden border border-gray-100 hover:border-cyan-400/50 hover:shadow-xl hover:shadow-cyan-400/20 transition-all duration-300 transform hover:-translate-y-1">
          <a href="https://irip.camsmesystem.com/login" target="_blank"
            class="block h-48 bg-white flex items-center justify-center relative overflow-hidden p-4">
            <img :src="'/irip.png'" alt="IRIP Project"
              class="w-full h-full object-contain group-hover:scale-105 transition-transform duration-500" />
            <div class="absolute inset-0 bg-black/10 group-hover:bg-black/0 transition-colors"></div>
          </a>
          <div class="p-8 flex flex-col h-[calc(100%-12rem)]">
            <h3 class="text-xl font-bold text-content mb-3 group-hover:text-cyan-600 transition-colors">IRIP Platform
            </h3>
            <p class="text-content-light text-sm leading-relaxed mb-6 flex-grow">
              Investment Readiness Intelligence Platform. A freelance project focused on delivering a robust
              intelligence and assessment platform.
            </p>
            <div class="flex flex-wrap gap-2 mb-6">
              <span
                class="px-3 py-1 bg-cyan-50 text-xs font-medium text-cyan-700 rounded-full border border-cyan-100">Vue.js</span>
              <span
                class="px-3 py-1 bg-cyan-50 text-xs font-medium text-cyan-700 rounded-full border border-cyan-100">Web
                App</span>
            </div>
            <a href="https://irip.camsmesystem.com/login" target="_blank"
              class="inline-flex items-center text-cyan-600 text-sm font-bold hover:text-cyan-500 transition-colors mt-auto">
              Visit IRIP
              <ArrowRight class="w-4 h-4 ml-2 group-hover:translate-x-1 transition-transform" />
            </a>
          </div>
        </div>

        <!-- Project 2: GrowTokyo -->
        <div
          class="group bg-white rounded-2xl overflow-hidden border border-gray-100 hover:border-cyan-400/50 hover:shadow-xl hover:shadow-cyan-400/20 transition-all duration-300 transform hover:-translate-y-1">
          <a href="https://play.google.com/store/apps/details?id=com.growtokyo" target="_blank"
            class="block h-48 bg-white flex items-center justify-center relative overflow-hidden">
            <img :src="'/growtokyo.png'" alt="GrowTokyo App"
              class="w-full h-full object-contain p-4 group-hover:scale-105 transition-transform duration-500" />
            <div class="absolute inset-0 bg-black/10 group-hover:bg-black/0 transition-colors"></div>
          </a>
          <div class="p-8 flex flex-col h-[calc(100%-12rem)]">
            <h3 class="text-xl font-bold text-content mb-3 group-hover:text-cyan-600 transition-colors">GrowTokyo Hair
              Salon</h3>
            <p class="text-content-light text-sm leading-relaxed mb-6 flex-grow">
              A complete production mobile application for a premium hair salon, available on the Google Play Store.
            </p>
            <div class="flex flex-wrap gap-2 mb-6">
              <span
                class="px-3 py-1 bg-cyan-50 text-xs font-medium text-cyan-700 rounded-full border border-cyan-100">Mobile
                App</span>
              <span
                class="px-3 py-1 bg-cyan-50 text-xs font-medium text-cyan-700 rounded-full border border-cyan-100">Production</span>
            </div>
            <a href="https://play.google.com/store/apps/details?id=com.growtokyo" target="_blank"
              class="inline-flex items-center text-cyan-600 text-sm font-bold hover:text-cyan-500 transition-colors mt-auto">
              View on Play Store
              <ArrowRight class="w-4 h-4 ml-2 group-hover:translate-x-1 transition-transform" />
            </a>
          </div>
        </div>

        <!-- Project 3: Daishin -->
        <div
          class="group bg-white rounded-2xl overflow-hidden border border-gray-100 hover:border-cyan-400/50 hover:shadow-xl hover:shadow-cyan-400/20 transition-all duration-300 transform hover:-translate-y-1">
          <a href="#" class="block h-48 bg-white flex items-center justify-center relative overflow-hidden">
            <img :src="'/daishin.png'" alt="Daishin Trading"
              class="w-full h-full object-contain p-4 group-hover:scale-105 transition-transform duration-500" />
            <div class="absolute inset-0 bg-black/5 group-hover:bg-black/0 transition-colors"></div>
          </a>
          <div class="p-8 flex flex-col h-[calc(100%-12rem)]">
            <h3 class="text-xl font-bold text-content mb-3 group-hover:text-cyan-600 transition-colors">Daishin & Our
              Pharmacy</h3>
            <p class="text-content-light text-sm leading-relaxed mb-6 flex-grow">
              A nearly complete production application for Daishin Trading and the Our Pharmacy platform.
            </p>
            <div class="flex flex-wrap gap-2 mb-6">
              <span
                class="px-3 py-1 bg-cyan-50 text-xs font-medium text-cyan-700 rounded-full border border-cyan-100">Enterprise</span>
              <span
                class="px-3 py-1 bg-cyan-50 text-xs font-medium text-cyan-700 rounded-full border border-cyan-100">Production</span>
            </div>
            <a href="#"
              class="inline-flex items-center text-cyan-600 text-sm font-bold hover:text-cyan-500 transition-colors mt-auto">
              Coming Soon
              <ArrowRight class="w-4 h-4 ml-2 group-hover:translate-x-1 transition-transform" />
            </a>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ArrowRight } from 'lucide-vue-next'
</script>
