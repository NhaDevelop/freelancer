<template>
  <section id="home" class="min-h-screen flex items-center relative overflow-hidden pt-20 bg-background">
    <!-- Subtle Gradient Backdrop -->
    <div class="absolute top-0 right-0 w-[800px] h-[800px] bg-secondary/5 rounded-full blur-[120px] -translate-y-1/2 translate-x-1/2 -z-10 pointer-events-none"></div>

    <div class="container mx-auto px-6 relative z-10 w-full">
      <div class="grid lg:grid-cols-2 gap-12 lg:gap-20 items-center">
        
        <!-- Left Column: Content -->
        <div class="max-w-2xl">
          <div class="inline-flex items-center gap-2 px-3 py-1 rounded-full bg-primary/10 text-primary text-xs font-bold uppercase tracking-widest mb-8">
            <span class="w-2 h-2 rounded-full bg-primary animate-pulse"></span>
            Available for new projects
          </div>
          
          <h1 class="text-5xl lg:text-7xl font-bold text-content tracking-tight leading-tight mb-8">
            Building Scalable <span class="text-primary">Digital Future</span>
          </h1>
          
          <p class="text-lg text-content-light leading-relaxed mb-10 max-w-xl">
            We are The Dev Quartet. A specialized team of senior engineers delivering enterprise-grade web and mobile applications with precision and speed.
          </p>

          <div class="flex flex-col sm:flex-row gap-4 mb-16">
            <a href="#contact" class="px-8 py-4 rounded-xl bg-primary hover:bg-primary-hover text-white font-semibold shadow-lg shadow-primary/25 hover:shadow-primary/40 transform hover:-translate-y-1 transition-all duration-300 text-center">
              Start Your Project
            </a>
            <a href="#work" class="px-8 py-4 rounded-xl bg-white border border-gray-200 hover:border-primary text-content hover:text-primary font-semibold hover:shadow-md transition-all duration-300 text-center flex items-center justify-center gap-2">
              View Our Work
              <ArrowRight class="w-4 h-4" />
            </a>
          </div>

          <!-- Trust Indicators -->
          <div class="pt-8 border-t border-gray-200">
            <p class="text-xs font-semibold text-content-light uppercase tracking-wider mb-4">Trusted Technologies</p>
            <div class="flex gap-8 opacity-50 grayscale hover:grayscale-0 transition-all duration-500">
               <!-- Simple generic tech logos for 'Trust' visual -->
               <Layers class="w-8 h-8" />
               <Database class="w-8 h-8" />
               <Cloud class="w-8 h-8" />
               <ShieldCheck class="w-8 h-8" />
               <Globe class="w-8 h-8" />
            </div>
          </div>
        </div>

        <!-- Right Column: Visual (Abstract Code Window) -->
        <div class="relative hidden lg:block">
          <!-- Clean structured shadow instead of blurred glow -->
          <div class="absolute -inset-2 bg-secondary/10 rounded-2xl -z-10 translate-x-2 translate-y-2"></div>
          
          <div class="relative bg-white rounded-2xl border border-gray-200 shadow-2xl overflow-hidden transform rotate-1 hover:rotate-0 transition-transform duration-500">
            <!-- Window Header -->
            <div class="bg-gray-50 border-b border-gray-200 px-4 py-3 flex items-center gap-2">
              <div class="flex gap-1.5">
                <div class="w-3 h-3 rounded-full bg-gray-300"></div>
                <div class="w-3 h-3 rounded-full bg-gray-300"></div>
                <div class="w-3 h-3 rounded-full bg-gray-300"></div>
              </div>
              <div class="text-xs text-gray-400 font-mono ml-4">Agency.ts</div>
            </div>
            <!-- Code Content -->
            <div class="p-6 font-mono text-xs sm:text-sm leading-relaxed text-slate-600 bg-white">
              <p><span class="text-purple-600">interface</span> <span class="text-yellow-600">Agency</span> {</p>
              <p class="pl-4"><span class="text-slate-500">name</span>: <span class="text-green-600">'The Dev Quartet'</span>;</p>
              <p class="pl-4"><span class="text-slate-500">expertise</span>: [<span class="text-green-600">'Web'</span>, <span class="text-green-600">'Mobile'</span>, <span class="text-green-600">'Cloud'</span>];</p>
              <p class="pl-4"><span class="text-slate-500">mission</span>: <span class="text-green-600">'Deliver Excellence'</span>;</p>
              
              <p class="pl-4 mt-2"><span class="text-purple-600">async</span> <span class="text-blue-600">buildFuture</span>() {</p>
              <p class="pl-8"><span class="text-purple-600">await</span> <span class="text-red-500">this</span>.<span class="text-blue-600">analyze</span>();</p>
              <p class="pl-8"><span class="text-purple-600">return</span> <span class="text-purple-600">new</span> <span class="text-yellow-600">Solution</span>({</p>
              <p class="pl-12"><span class="text-slate-500">quality</span>: <span class="text-orange-500">MAX_INT</span>,</p>
              <p class="pl-12"><span class="text-slate-500">deadline</span>: <span class="text-orange-500">MET</span></p>
              <p class="pl-8">});</p>
              <p class="pl-4">}</p>
              <p>}</p>
            </div>
          </div>
        </div>

      </div>
    </div>
  </section>
</template>

<script setup>
import { ArrowRight, Layers, Database, Cloud, ShieldCheck, Globe } from 'lucide-vue-next'
</script>
