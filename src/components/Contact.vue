<template>
  <footer id="contact" class="pt-24 pb-12 border-t border-gray-200 bg-white">
    <div class="container mx-auto px-6">
      
      <!-- Top Section: CTA + Links -->
      <div class="grid lg:grid-cols-4 gap-12 mb-20">
        
        <!-- Brand / About -->
        <div class="lg:col-span-1">
          <h3 class="text-xl font-bold text-content mb-6 tracking-tight">The Dev Quartet</h3>
          <p class="text-content-light text-sm leading-relaxed mb-8">
            Empowering businesses with enterprise-grade software solutions.
          </p>
          <div class="flex gap-3">
             <a href="#" class="w-9 h-9 rounded-lg bg-gray-50 border border-gray-200 flex items-center justify-center text-content-light hover:bg-primary hover:text-white hover:border-primary transition-all duration-300">
               <Github class="w-4 h-4" />
             </a>
             <a href="#" class="w-9 h-9 rounded-lg bg-gray-50 border border-gray-200 flex items-center justify-center text-content-light hover:bg-primary hover:text-white hover:border-primary transition-all duration-300">
               <Linkedin class="w-4 h-4" />
             </a>
             <a href="#" class="w-9 h-9 rounded-lg bg-gray-50 border border-gray-200 flex items-center justify-center text-content-light hover:bg-primary hover:text-white hover:border-primary transition-all duration-300">
               <Twitter class="w-4 h-4" />
             </a>
          </div>
        </div>

        <!-- Links Cols -->
        <div>
          <h4 class="font-bold text-content mb-6 text-sm uppercase tracking-wider">Company</h4>
          <ul class="space-y-4 text-sm text-content-light">
            <li><a href="#home" class="hover:text-primary transition-colors">About Us</a></li>
            <li><a href="#team" class="hover:text-primary transition-colors">Leadership</a></li>
            <li><a href="#" class="hover:text-primary transition-colors">Careers</a></li>
          </ul>
        </div>

         <div>
          <h4 class="font-bold text-content mb-6 text-sm uppercase tracking-wider">Services</h4>
          <ul class="space-y-4 text-sm text-content-light">
            <li><a href="#services" class="hover:text-primary transition-colors">Web Development</a></li>
            <li><a href="#services" class="hover:text-primary transition-colors">Mobile Solutions</a></li>
            <li><a href="#services" class="hover:text-primary transition-colors">Cloud Architecture</a></li>
          </ul>
        </div>

        <!-- Contact Detailed -->
        <div>
          <h4 class="font-bold text-content mb-6 text-sm uppercase tracking-wider">Contact</h4>
          <ul class="space-y-4 text-sm text-content-light">
            <li class="flex items-start gap-3">
              <Mail class="w-4 h-4 text-primary mt-1" />
              <span>hello@devquartet.com</span>
            </li>
            <li class="flex items-start gap-3">
              <Phone class="w-4 h-4 text-primary mt-1" />
              <span>+1 (555) 000-0000</span>
            </li>
            <li class="flex items-start gap-3">
              <MapPin class="w-4 h-4 text-primary mt-1" />
              <span>San Francisco, CA<br>Available Worldwide</span>
            </li>
          </ul>
        </div>

      </div>

      <!-- Bottom Bar -->
      <div class="border-t border-gray-100 pt-8 flex flex-col md:flex-row justify-between items-center gap-4 text-xs text-content-light">
        <p>&copy; {{ new Date().getFullYear() }} The Dev Quartet. All rights reserved.</p>
        <div class="flex gap-6">
          <a href="#" class="hover:text-primary transition-colors">Privacy Policy</a>
          <a href="#" class="hover:text-primary transition-colors">Terms of Service</a>
        </div>
      </div>
    </div>
  </footer>
</template>

<script setup>
import { Github, Linkedin, Twitter, Mail, Phone, MapPin } from 'lucide-vue-next'
</script>
