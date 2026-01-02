<template>
  <div class="min-h-screen bg-dark-bg">
    <Navbar />
    <Hero />
    <TeamSection />
    <TechStack />
    <Services />
    <Contact />
  </div>
</template>

<script setup>
import Navbar from './components/Navbar.vue'
import Hero from './components/Hero.vue'
import TeamSection from './components/TeamSection.vue'
import TechStack from './components/TechStack.vue'
import Services from './components/Services.vue'
import Contact from './components/Contact.vue'
</script>
