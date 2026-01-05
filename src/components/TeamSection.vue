<template>
  <section id="team" class="py-20 bg-background relative overflow-hidden">
    <!-- Clean Background with subtle tint -->
    <div class="absolute bottom-0 left-0 w-[600px] h-[600px] bg-secondary/3 rounded-full blur-[100px] -translate-x-1/3 translate-y-1/3 -z-10 pointer-events-none"></div>

    <div class="container mx-auto px-6 relative z-10">
      <div class="text-center mb-16">
        <span class="text-primary font-bold tracking-widest uppercase text-xs mb-4 block">Our Team</span>
        <h2 class="text-3xl md:text-4xl font-bold text-content mb-6">
          Meet the <span class="text-primary">Experts</span>
        </h2>
        <p class="text-content-light max-w-2xl mx-auto text-lg leading-relaxed">
          Senior-level engineers dedicated to your project's success.
        </p>
      </div>

      <!-- Team Grid - Fixed to show all 4 cards -->
      <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-6">
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
