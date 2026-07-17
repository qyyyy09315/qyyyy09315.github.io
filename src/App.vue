<template>
  <div class="app">
    <NavBar :current-section="currentPage" @navigate="scrollTo" />
    <main class="scroll-container">
      <section
        v-for="(section, index) in sections"
        :key="section.id"
        :id="section.id"
        ref="sectionRefs"
        class="full-page-section"
      >
        <component :is="section.component" />
      </section>
    </main>
  </div>
</template>

<script setup>
import { ref, provide, onMounted, onUnmounted, shallowRef } from 'vue'

import NavBar from './components/NavBar.vue'
import HeroSection from './components/HeroSection.vue'
import AboutSection from './components/AboutSection.vue'
import SkillsSection from './components/SkillsSection.vue'
import ProjectsSection from './components/ProjectsSection.vue'
import EducationSection from './components/EducationSection.vue'
import ContactSection from './components/ContactSection.vue'
import FooterSection from './components/FooterSection.vue'

const sections = shallowRef([
  { id: 'hero', component: HeroSection },
  { id: 'about', component: AboutSection },
  { id: 'skills', component: SkillsSection },
  { id: 'projects', component: ProjectsSection },
  { id: 'education', component: EducationSection },
  { id: 'contact', component: ContactSection },
  { id: 'footer', component: FooterSection }
])

const currentPage = ref(0)
const isScrolling = ref(false)
const sectionRefs = ref([])
const container = ref(null)

const scrollTo = (index) => {
  if (index < 0 || index >= sections.value.length || isScrolling.value) return
  isScrolling.value = true
  currentPage.value = index
  sectionRefs.value[index]?.scrollIntoView({ behavior: 'smooth' })
  setTimeout(() => { isScrolling.value = false }, 100)
}

provide('navigateTo', scrollTo)

const setVH = () => {
  const vh = window.innerHeight * 0.01
  document.documentElement.style.setProperty('--vh', `${vh}px`)
}

const handleWheel = (e) => {
  if (isMobile()) return
  if (isScrolling.value) {
    e.preventDefault()
    return
  }
  e.preventDefault()
  if (e.deltaY > 0) {
    scrollTo(currentPage.value + 1)
  } else if (e.deltaY < 0) {
    scrollTo(currentPage.value - 1)
  }
}

const handleKey = (e) => {
  if (isScrolling.value) return
  if (e.key === 'ArrowDown' || e.key === 'PageDown') {
    e.preventDefault()
    scrollTo(currentPage.value + 1)
  } else if (e.key === 'ArrowUp' || e.key === 'PageUp') {
    e.preventDefault()
    scrollTo(currentPage.value - 1)
  }
}

const isMobile = () => window.innerWidth <= 768

let touchStartY = 0
const handleTouchStart = (e) => {
  if (isMobile()) return
  touchStartY = e.touches[0].clientY
}
const handleTouchEnd = (e) => {
  if (isMobile()) return
  const diff = touchStartY - e.changedTouches[0].clientY
  if (Math.abs(diff) > 50) {
    if (diff > 0) scrollTo(currentPage.value + 1)
    else scrollTo(currentPage.value - 1)
  }
}

onMounted(() => {
  setVH()
  window.addEventListener('resize', setVH)
  window.addEventListener('orientationchange', setVH)
  window.addEventListener('wheel', handleWheel, { passive: false })
  window.addEventListener('keydown', handleKey)
  window.addEventListener('touchstart', handleTouchStart, { passive: true })
  window.addEventListener('touchend', handleTouchEnd, { passive: true })
})

onUnmounted(() => {
  window.removeEventListener('resize', setVH)
  window.removeEventListener('orientationchange', setVH)
  window.removeEventListener('wheel', handleWheel)
  window.removeEventListener('keydown', handleKey)
  window.removeEventListener('touchstart', handleTouchStart)
  window.removeEventListener('touchend', handleTouchEnd)
})
</script>

<style scoped>
.app {
  width: 100%;
  overflow-x: hidden;
}

.scroll-container {
  width: 100%;
}

.full-page-section {
  display: flex;
  flex-direction: column;
  justify-content: center;
  min-height: 100vh;
  min-height: calc(var(--vh, 1vh) * 100);
  scroll-snap-align: start;
}

@media (max-width: 768px) {
  .scroll-container {
    height: auto;
    overflow: visible;
  }

  .full-page-section {
    height: auto;
    min-height: calc(var(--vh) * 100);
    justify-content: flex-start;
  }

  .full-page-section:first-child {
    min-height: auto;
  }
}
</style>
