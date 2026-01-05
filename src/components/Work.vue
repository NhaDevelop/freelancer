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
        <!-- Project 1 -->
        <div class="group bg-white rounded-2xl overflow-hidden border border-gray-100 hover:border-cyan-400/50 hover:shadow-xl hover:shadow-cyan-400/20 transition-all duration-300 transform hover:-translate-y-1">
          <div class="h-48 bg-gray-100 flex items-center justify-center relative overflow-hidden group-hover:opacity-90 transition-opacity">
            <img src="file:///Users/user/.gemini/antigravity/brain/438c6c15-04b6-4ef7-b9ac-2db7238e238a/fintech_dashboard_mockup_1767451932819.png" alt="Fintech Dashboard" class="w-full h-full object-cover">
          </div>
          <div class="p-8">
            <h3 class="text-xl font-bold text-content mb-3 group-hover:text-cyan-600 transition-colors">NeoBank Platform</h3>
            <p class="text-content-light text-sm leading-relaxed mb-6">
              A high-performance banking dashboard handling real-time transactions and data visualization.
            </p>
            <div class="flex flex-wrap gap-2 mb-6">
              <span class="px-3 py-1 bg-cyan-50 text-xs font-medium text-cyan-700 rounded-full border border-cyan-100">Vue.js</span>
              <span class="px-3 py-1 bg-cyan-50 text-xs font-medium text-cyan-700 rounded-full border border-cyan-100">D3.js</span>
              <span class="px-3 py-1 bg-cyan-50 text-xs font-medium text-cyan-700 rounded-full border border-cyan-100">TypeScript</span>
            </div>
            <a href="#" class="inline-flex items-center text-cyan-600 text-sm font-bold hover:text-cyan-500 transition-colors">
              View Case Study <ArrowRight class="w-4 h-4 ml-2 group-hover:translate-x-1 transition-transform" />
            </a>
          </div>
        </div>

        <!-- Project 2 -->
        <div class="group bg-white rounded-2xl overflow-hidden border border-gray-100 hover:border-cyan-400/50 hover:shadow-xl hover:shadow-cyan-400/20 transition-all duration-300 transform hover:-translate-y-1">
          <div class="h-48 bg-gray-100 flex items-center justify-center relative overflow-hidden group-hover:opacity-90 transition-opacity">
            <img src="file:///Users/user/.gemini/antigravity/brain/438c6c15-04b6-4ef7-b9ac-2db7238e238a/fashion_store_mockup_1767451957792.png" alt="Luxury Fashion App" class="w-full h-full object-cover">
          </div>
          <div class="p-8">
            <h3 class="text-xl font-bold text-content mb-3 group-hover:text-cyan-600 transition-colors">Luxe Fashion Store</h3>
            <p class="text-content-light text-sm leading-relaxed mb-6">
              A scalable headless e-commerce solution with sub-second page loads and seamless checkout.
            </p>
            <div class="flex flex-wrap gap-2 mb-6">
              <span class="px-3 py-1 bg-cyan-50 text-xs font-medium text-cyan-700 rounded-full border border-cyan-100">Next.js</span>
              <span class="px-3 py-1 bg-cyan-50 text-xs font-medium text-cyan-700 rounded-full border border-cyan-100">Shopify</span>
              <span class="px-3 py-1 bg-cyan-50 text-xs font-medium text-cyan-700 rounded-full border border-cyan-100">Tailwind</span>
            </div>
            <a href="#" class="inline-flex items-center text-cyan-600 text-sm font-bold hover:text-cyan-500 transition-colors">
              View Case Study <ArrowRight class="w-4 h-4 ml-2 group-hover:translate-x-1 transition-transform" />
            </a>
          </div>
        </div>

        <!-- Project 3 -->
        <div class="group bg-white rounded-2xl overflow-hidden border border-gray-100 hover:border-cyan-400/50 hover:shadow-xl hover:shadow-cyan-400/20 transition-all duration-300 transform hover:-translate-y-1">
          <div class="h-48 bg-gray-100 flex items-center justify-center relative overflow-hidden group-hover:opacity-90 transition-opacity">
             <img src="file:///Users/user/.gemini/antigravity/brain/438c6c15-04b6-4ef7-b9ac-2db7238e238a/saas_platform_mockup_1767451981122.png" alt="SaaS Platform" class="w-full h-full object-cover">
          </div>
          <div class="p-8">
            <h3 class="text-xl font-bold text-content mb-3 group-hover:text-cyan-600 transition-colors">TaskFlow Enterprise</h3>
            <p class="text-content-light text-sm leading-relaxed mb-6">
              Collaborative project management tool for enterprise teams with real-time sockets.
            </p>
            <div class="flex flex-wrap gap-2 mb-6">
              <span class="px-3 py-1 bg-cyan-50 text-xs font-medium text-cyan-700 rounded-full border border-cyan-100">React</span>
              <span class="px-3 py-1 bg-cyan-50 text-xs font-medium text-cyan-700 rounded-full border border-cyan-100">Node.js</span>
              <span class="px-3 py-1 bg-cyan-50 text-xs font-medium text-cyan-700 rounded-full border border-cyan-100">Socket.io</span>
            </div>
            <a href="#" class="inline-flex items-center text-cyan-600 text-sm font-bold hover:text-cyan-500 transition-colors">
              View Case Study <ArrowRight class="w-4 h-4 ml-2 group-hover:translate-x-1 transition-transform" />
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
