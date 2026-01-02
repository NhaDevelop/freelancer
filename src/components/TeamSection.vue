<template>
  <section id="team" class="py-24 relative overflow-hidden">
    <!-- Vibrant Background -->
    <div class="absolute inset-0 bg-gradient-to-br from-cyan-900/10 via-purple-900/10 to-pink-900/10"></div>
    
    <!-- Animated Orbs -->
    <div class="absolute top-40 left-10 w-80 h-80 bg-gradient-to-br from-cyan-400 to-blue-500 rounded-full blur-3xl opacity-20 animate-pulse"></div>
    <div class="absolute bottom-40 right-10 w-80 h-80 bg-gradient-to-br from-purple-400 to-pink-500 rounded-full blur-3xl opacity-20 animate-pulse" style="animation-delay: 1s;"></div>
    
    <div class="container mx-auto px-6 relative z-10">
      <!-- Section Header -->
      <div class="text-center mb-20">
        <h2 class="text-5xl md:text-6xl font-black mb-6 bg-gradient-to-r from-cyan-400 via-purple-400 to-pink-400 bg-clip-text text-transparent flex items-center justify-center gap-4">
          <Users class="w-12 h-12 text-cyan-400" :stroke-width="2.5" />
          Meet The Team
        </h2>
        <p class="text-gray-300 text-xl md:text-2xl max-w-3xl mx-auto font-medium leading-relaxed">
          Four <span class="text-cyan-400 font-bold">talented developers</span>, one 
          <span class="text-purple-400 font-bold">powerful collective</span>. 
          We combine our expertise to deliver 
          <span class="text-pink-400 font-bold">exceptional results</span>
        </p>
      </div>

      <!-- Team Grid - Fixed to show all 4 cards -->
      <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-6 md:gap-8">
        <TeamCard 
          v-for="member in teamMembers" 
          :key="member.id"
          :member="member"
        />
      </div>
    </div>
  </section>
</template>

<script setup>
import { Users } from 'lucide-vue-next'
import TeamCard from './TeamCard.vue'
import { teamMembers } from '../data/teamData'

console.log('Team members count:', teamMembers.length)
console.log('Team members:', teamMembers)
</script>
