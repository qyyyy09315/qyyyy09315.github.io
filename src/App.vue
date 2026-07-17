<template>
  <div class="app">
    <NavBar :current-section="currentPage" @navigate="scrollTo" />
    <main class="scroll-container" ref="scrollContainer">
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
import { ref, provide, onMounted, onUnmounted, shallowRef, nextTick } from 'vue'

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
const scrollContainer = ref(null)

// Custom smooth scroll using requestAnimationFrame
const smoothScrollTo = (targetY, duration = 600) => {
  const startY = window.scrollY
  const distance = targetY - startY
  const startTime = performance.now()

  const animate = (currentTime) => {
    const elapsed = currentTime - startTime
    const progress = Math.min(elapsed / duration, 1)
    // Ease out cubic
    const ease = 1 - Math.pow(1 - progress, 3)
    
    window.scrollTo(0, startY + distance * ease)
    
    if (progress < 1) {
      requestAnimationFrame(animate)
    } else {
      isScrolling.value = false
    }
  }

  requestAnimationFrame(animate)
}

const scrollTo = (index) => {
  if (index < 0 || index >= sections.value.length || isScrolling.value) return
  isScrolling.value = true
  currentPage.value = index
  
  nextTick(() => {
    const target = sectionRefs.value[index]
    if (target) {
      const rect = target.getBoundingClientRect()
      const targetY = window.scrollY + rect.top
      smoothScrollTo(targetY, 600)
    } else {
      isScrolling.value = false
    }
  })
}

provide('navigateTo', scrollTo)

const setVH = () => {
  const vh = window.innerHeight * 0.01
  document.documentElement.style.setProperty('--vh', `${vh}px`)
}

// Throttled wheel handler
let wheelTimeout = null
const handleWheel = (e) => {
  if (isMobile()) return
  e.preventDefault()
  
  if (wheelTimeout) return
  
  wheelTimeout = setTimeout(() => {
    wheelTimeout = null
  }, 800)
  
  if (isScrolling.value) return
  
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

// IntersectionObserver to trigger CSS animations
let animationObserver = null

onMounted(() => {
  setVH()
  window.addEventListener('resize', setVH)
  window.addEventListener('orientationchange', setVH)
  window.addEventListener('wheel', handleWheel, { passive: false })
  window.addEventListener('keydown', handleKey)
  window.addEventListener('touchstart', handleTouchStart, { passive: true })
  window.addEventListener('touchend', handleTouchEnd, { passive: true })

  // Single IntersectionObserver for all .animate elements
  animationObserver = new IntersectionObserver(
    (entries) => {
      entries.forEach((entry) => {
        if (entry.isIntersecting) {
          entry.target.classList.add('visible')
          animationObserver.unobserve(entry.target)
        }
      })
    },
    { threshold: 0.1, rootMargin: '0px 0px -40px 0px' }
  )

  // Observe all .animate elements after DOM is ready
  nextTick(() => {
    document.querySelectorAll('.animate').forEach((el) => {
      animationObserver.observe(el)
    })
  })
})

onUnmounted(() => {
  window.removeEventListener('resize', setVH)
  window.removeEventListener('orientationchange', setVH)
  window.removeEventListener('wheel', handleWheel)
  window.removeEventListener('keydown', handleKey)
  window.removeEventListener('touchstart', handleTouchStart)
  window.removeEventListener('touchend', handleTouchEnd)
  if (animationObserver) animationObserver.disconnect()
})
</script>

<style scoped>
.app {
  width: 100%;
  overflow-x: hidden;
}

.scroll-container {
  width: 100%;
  /* CSS scroll snap - GPU accelerated */
  scroll-snap-type: y mandatory;
  scroll-behavior: smooth;
  overflow-y: scroll;
  height: 100vh;
  height: calc(var(--vh, 1vh) * 100);
}

.full-page-section {
  display: flex;
  flex-direction: column;
  justify-content: center;
  min-height: 100vh;
  min-height: calc(var(--vh, 1vh) * 100);
  scroll-snap-align: start;
  /* GPU acceleration for sections */
  will-change: transform;
  contain: layout style paint;
}

@media (max-width: 768px) {
  .scroll-container {
    height: auto;
    overflow: visible;
    scroll-snap-type: none;
    scroll-behavior: auto;
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
