<template>
  <nav class="navbar" :class="{ 'navbar-scrolled': isScrolled }">
    <div class="nav-inner">
      <a href="#" class="nav-logo" @click.prevent="$emit('navigate', 0)">
        <span class="logo-bracket">&lt;</span>Yue-xin G.<span class="logo-bracket">/&gt;</span>
      </a>

      <ul class="nav-links">
        <li v-for="(link, idx) in links" :key="idx">
          <a
            :href="link.href"
            :class="{ active: currentSection === link.index }"
            @click.prevent="$emit('navigate', link.index)"
          >
            <span class="link-number">{{ String(idx + 1).padStart(2, '0') }}</span>
            {{ link.label }}
          </a>
        </li>
      </ul>
    </div>
  </nav>
</template>

<script setup>
import { ref, onMounted, onUnmounted } from 'vue'

defineProps({
  currentSection: { type: Number, default: 0 }
})
defineEmits(['navigate'])

const links = [
  { label: 'About', href: '#about', index: 1 },
  { label: 'Skills', href: '#skills', index: 2 },
  { label: 'Education', href: '#education', index: 3 },
  { label: 'Contact', href: '#contact', index: 4 }
]

const isScrolled = ref(false)

const handleScroll = () => {
  isScrolled.value = window.scrollY > 50
}

onMounted(() => {
  window.addEventListener('scroll', handleScroll, { passive: true })
})

onUnmounted(() => {
  window.removeEventListener('scroll', handleScroll)
})
</script>

<style scoped>
.navbar {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  z-index: 100;
  transition: all var(--duration-normal) var(--ease-out);
}

.navbar-scrolled {
  background: rgba(255, 255, 255, 0.88);
  backdrop-filter: blur(16px);
  border-bottom: 1px solid var(--border-subtle);
}

.nav-inner {
  max-width: 1120px;
  margin: 0 auto;
  padding: 0 2rem;
  height: 64px;
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.nav-logo {
  font-family: var(--font-mono);
  font-size: 0.875rem;
  font-weight: 500;
  color: var(--text);
  text-decoration: none;
  letter-spacing: -0.02em;
}

.logo-bracket {
  color: var(--accent);
  opacity: 0.6;
}

.nav-links {
  display: flex;
  gap: 0.25rem;
  list-style: none;
  margin: 0;
  padding: 0;
}

.nav-links a {
  display: flex;
  align-items: center;
  gap: 0.375rem;
  padding: 0.5rem 0.75rem;
  color: var(--text-muted);
  text-decoration: none;
  font-size: 0.8125rem;
  font-weight: 500;
  border-radius: 6px;
  transition: all var(--duration-fast) var(--ease-out);
}

.nav-links a:hover {
  color: var(--text);
  background: var(--bg-subtle);
}

.nav-links a.active {
  color: var(--accent);
  background: var(--accent-subtle);
}

.link-number {
  font-family: var(--font-mono);
  font-size: 0.6875rem;
  opacity: 0.6;
}

@media (max-width: 640px) {
  .nav-links {
    display: none;
  }

  .nav-inner {
    padding: 0 1.5rem;
  }
}
</style>
