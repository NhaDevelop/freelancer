<template>
  <section id="home" class="min-h-screen flex items-center justify-center relative overflow-hidden pt-20">
    <!-- Vibrant Background Orbs -->
    <div class="absolute inset-0 overflow-hidden pointer-events-none">
      <div class="absolute top-20 left-10 w-96 h-96 bg-cyan-500/20 rounded-full blur-3xl animate-pulse"></div>
      <div class="absolute bottom-20 right-10 w-[500px] h-[500px] bg-purple-500/20 rounded-full blur-3xl animate-pulse" style="animation-delay: 1s;"></div>
      <div class="absolute top-1/2 left-1/2 w-96 h-96 bg-pink-500/20 rounded-full blur-3xl animate-pulse" style="animation-delay: 2s;"></div>
    </div>

    <!-- Content -->
    <div class="container mx-auto px-6 relative z-10">
      <div class="text-center max-w-6xl mx-auto">
        <!-- Main Heading -->
        <h1 class="text-5xl md:text-7xl lg:text-8xl font-black mb-8 leading-tight" ref="heroTitle">
          <span class="block mb-4 bg-gradient-to-r from-cyan-400 via-purple-400 to-pink-400 bg-clip-text text-transparent">
            Full-Stack Excellence
          </span>
          <span class="text-white text-4xl md:text-6xl lg:text-7xl">Meets Mobile Innovation</span>
        </h1>

        <!-- Subtitle -->
        <p class="text-xl md:text-2xl lg:text-3xl text-gray-200 mb-12 max-w-4xl mx-auto leading-relaxed font-medium" ref="heroSubtitle">
          We're a collective of <span class="text-cyan-400 font-bold">elite developers</span> crafting 
          <span class="text-purple-400 font-bold">cutting-edge</span> web and mobile solutions 🚀
        </p>

        <!-- CTA Buttons -->
        <div class="flex flex-col sm:flex-row gap-6 justify-center items-center mb-20" ref="heroButtons">
          <a href="#services" class="px-8 py-4 rounded-full bg-gradient-to-r from-cyan-500 to-purple-500 text-white font-bold text-lg hover:scale-105 hover:shadow-2xl hover:shadow-cyan-500/50 transition-all duration-300">
            🎯 Explore Our Services
          </a>
          <a href="#team" class="px-8 py-4 rounded-full border-3 border-cyan-400 text-cyan-400 font-bold text-lg hover:bg-cyan-400 hover:text-gray-900 hover:scale-105 transition-all duration-300">
            👥 Meet The Team
          </a>
        </div>

        <!-- Stats Cards -->
        <div class="grid grid-cols-2 md:grid-cols-4 gap-6" ref="heroStats">
          <div class="bg-white/10 backdrop-blur-lg border-2 border-white/20 rounded-2xl p-8 hover:bg-white/20 hover:shadow-2xl hover:shadow-cyan-500/30 transition-all">
            <div class="text-5xl font-black mb-3 bg-gradient-to-r from-cyan-400 to-blue-500 bg-clip-text text-transparent">11+</div>
            <div class="text-gray-300 font-semibold text-lg">Technologies</div>
          </div>
          <div class="bg-white/10 backdrop-blur-lg border-2 border-white/20 rounded-2xl p-8 hover:bg-white/20 hover:shadow-2xl hover:shadow-purple-500/30 transition-all">
            <div class="text-5xl font-black mb-3 bg-gradient-to-r from-purple-400 to-pink-500 bg-clip-text text-transparent">4</div>
            <div class="text-gray-300 font-semibold text-lg">Expert Developers</div>
          </div>
          <div class="bg-white/10 backdrop-blur-lg border-2 border-white/20 rounded-2xl p-8 hover:bg-white/20 hover:shadow-2xl hover:shadow-green-500/30 transition-all">
            <div class="text-5xl font-black mb-3 bg-gradient-to-r from-green-400 to-emerald-500 bg-clip-text text-transparent">100%</div>
            <div class="text-gray-300 font-semibold text-lg">Commitment</div>
          </div>
          <div class="bg-white/10 backdrop-blur-lg border-2 border-white/20 rounded-2xl p-8 hover:bg-white/20 hover:shadow-2xl hover:shadow-orange-500/30 transition-all">
            <div class="text-5xl font-black mb-3 bg-gradient-to-r from-orange-400 to-red-500 bg-clip-text text-transparent">24/7</div>
            <div class="text-gray-300 font-semibold text-lg">Support</div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref, onMounted } from 'vue'
import { gsap } from 'gsap'

const heroTitle = ref(null)
const heroSubtitle = ref(null)
const heroButtons = ref(null)
const heroStats = ref(null)

onMounted(() => {
  const timeline = gsap.timeline()
  
  timeline
    .from(heroTitle.value, {
      opacity: 0,
      y: 80,
      duration: 1.2,
      ease: 'power4.out'
    })
    .from(heroSubtitle.value, {
      opacity: 0,
      y: 50,
      duration: 1,
      ease: 'power3.out'
    }, '-=0.6')
    .from(heroButtons.value, {
      opacity: 0,
      y: 30,
      duration: 0.8,
      ease: 'power3.out'
    }, '-=0.5')
    .from(heroStats.value.children, {
      opacity: 0,
      y: 40,
      scale: 0.8,
      duration: 0.8,
      stagger: 0.15,
      ease: 'back.out(1.7)'
    }, '-=0.4')
})
</script>
