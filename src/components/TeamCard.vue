<template>
  <div class="bg-white/10 backdrop-blur-lg border-2 border-white/20 rounded-2xl p-8 text-center hover:bg-white/20 hover:border-cyan-400/50 hover:shadow-2xl hover:shadow-cyan-500/30 hover:-translate-y-2 hover:scale-105 transition-all duration-300">
    <!-- Avatar with Icon -->
    <div class="relative inline-block mb-6">
      <div class="w-32 h-32 mx-auto rounded-full bg-gradient-to-br from-cyan-400 via-purple-500 to-pink-500 flex items-center justify-center shadow-2xl hover:rotate-6 transition-transform duration-300">
        <component :is="getIcon(member.role)" class="w-16 h-16 text-white" :stroke-width="2" />
      </div>
    </div>

    <!-- Name -->
    <h3 class="text-3xl font-black mb-3 bg-gradient-to-r from-cyan-400 via-purple-400 to-pink-400 bg-clip-text text-transparent">
      {{ member.name }}
    </h3>

    <!-- Role -->
    <div class="inline-block px-6 py-2 rounded-full bg-gradient-to-r from-cyan-500 to-purple-500 mb-4 shadow-lg">
      <p class="text-white font-bold text-lg">
        {{ member.role }}
      </p>
    </div>

    <!-- Description -->
    <p class="text-gray-300 mb-6 text-base leading-relaxed">
      {{ member.description }}
    </p>

    <!-- Specializations -->
    <div class="flex flex-wrap gap-3 justify-center mb-6">
      <span 
        v-for="(spec, index) in member.specializations" 
        :key="index"
        class="px-4 py-2 rounded-full text-sm font-semibold bg-gradient-to-r text-white shadow-lg hover:scale-110 transition-transform"
        :class="index % 4 === 0 ? 'from-cyan-500 to-blue-500' : index % 4 === 1 ? 'from-purple-500 to-pink-500' : index % 4 === 2 ? 'from-green-500 to-emerald-500' : 'from-orange-500 to-red-500'"
      >
        {{ spec }}
      </span>
    </div>

    <!-- Social Links -->
    <div class="flex gap-5 justify-center">
      <a 
        :href="member.social.github" 
        class="w-12 h-12 rounded-full bg-gray-800 flex items-center justify-center hover:bg-cyan-500 transition-all duration-300 hover:scale-125 shadow-lg"
      >
        <Github class="w-6 h-6 text-white" />
      </a>
      <a 
        :href="member.social.linkedin" 
        class="w-12 h-12 rounded-full bg-blue-700 flex items-center justify-center hover:bg-purple-500 transition-all duration-300 hover:scale-125 shadow-lg"
      >
        <Linkedin class="w-6 h-6 text-white" />
      </a>
      <a 
        :href="member.social.twitter" 
        class="w-12 h-12 rounded-full bg-cyan-500 flex items-center justify-center hover:bg-green-500 transition-all duration-300 hover:scale-125 shadow-lg"
      >
        <Twitter class="w-6 h-6 text-white" />
      </a>
    </div>
  </div>
</template>

<script setup>
import { Github, Linkedin, Twitter, Briefcase, Zap, Smartphone, Palette } from 'lucide-vue-next'

defineProps({
  member: {
    type: Object,
    required: true
  }
})

const getIcon = (role) => {
  if (role.includes('Architect') || role.includes('Solutions')) return Briefcase
  if (role.includes('Backend') || role.includes('Engineer')) return Zap
  if (role.includes('Mobile')) return Smartphone
  if (role.includes('Frontend') || role.includes('Innovation')) return Palette
  return Briefcase
}
</script>
