<template>
  <div class="app">
    <NavBar />
    <main>
      <HeroSection />
      <AboutSection />
      <SkillsSection />
      <EducationSection />
      <ContactSection />
    </main>
    <FooterSection />
  </div>
</template>

<script setup>
import NavBar from './components/NavBar.vue'
import HeroSection from './components/HeroSection.vue'
import AboutSection from './components/AboutSection.vue'
import SkillsSection from './components/SkillsSection.vue'
import EducationSection from './components/EducationSection.vue'
import ContactSection from './components/ContactSection.vue'
import FooterSection from './components/FooterSection.vue'
</script>

<style scoped>
.app {
  min-height: 100vh;
}
</style>