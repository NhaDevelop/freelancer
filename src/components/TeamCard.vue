<template>
  <div class="group relative bg-white border border-gray-200 rounded-2xl p-6 transition-all duration-500 hover:shadow-xl hover:shadow-cyan-400/20 hover:border-cyan-400/50 hover:-translate-y-2 overflow-hidden">
    
    <div class="relative z-10 flex flex-col items-center text-center h-full">
      <!-- Member Icon (Placeholder for Photo) -->
      <div 
        class="w-24 h-24 rounded-full flex items-center justify-center mb-6 bg-gray-50 border border-gray-100 group-hover:border-cyan-400/50 transition-all duration-300"
      >
        <component :is="roleIcon" class="w-10 h-10 text-cyan-500 opacity-80" />
      </div>

      <!-- Member Info -->
      <h3 class="text-xl font-bold text-content mb-1">
        {{ member.name }}
      </h3>
      <p class="text-primary text-sm font-semibold tracking-wide uppercase mb-4">{{ member.role }}</p>
      
      <p class="text-content-light text-sm leading-relaxed mb-6 opacity-80 flex-grow">
        {{ member.description }}
      </p>

      <div class="border-t border-gray-100 w-full pt-4 mt-auto flex justify-center gap-5">
        <a 
          v-for="platform in Object.keys(member.social)" 
          :key="platform" 
          :href="member.social[platform]"
          target="_blank"
          class="text-gray-400 hover:text-primary transition-colors duration-300"
          :title="platform"
        >
          <component :is="getIcon(platform)" class="w-4 h-4" />
        </a>
      </div>
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

const roleIcon = Briefcase // Default fallback

const getIcon = (platform) => {
  if (platform === 'github') return Github
  if (platform === 'linkedin') return Linkedin
  if (platform === 'twitter') return Twitter
  return Twitter
}
</script>
