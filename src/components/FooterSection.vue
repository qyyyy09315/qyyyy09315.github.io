<template>
  <section id="footer" class="footer-section">
    <div class="content">
      <div class="footer-inner">
        <div class="footer-top">
          <div class="footer-brand">
            <span class="footer-logo">Yue-xin G.</span>
            <span class="footer-tagline">Building with data, learning with purpose.</span>
          </div>
          <div class="footer-nav">
            <a
              v-for="(link, idx) in navLinks"
              :key="idx"
              :href="link.href"
              @click.prevent="goTo(link.index)"
            >
              {{ link.label }}
            </a>
          </div>
        </div>

        <div class="footer-divider"></div>

        <div class="footer-bottom">
          <p class="footer-copy">&copy; {{ currentYear }} Yue-xin G. All rights reserved.</p>
          <p class="footer-built">Built with Vue 3 + Vite</p>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref, inject } from 'vue'

const currentYear = ref(new Date().getFullYear())
const goTo = inject('navigateTo', () => {})

const navLinks = [
  { label: 'About', href: '#about', index: 1 },
  { label: 'Skills', href: '#skills', index: 2 },
  { label: 'Education', href: '#education', index: 3 },
  { label: 'Contact', href: '#contact', index: 4 }
]
</script>

<style scoped>
.footer-section {
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  padding: 5rem 2rem;
  background: var(--text);
  color: var(--bg);
}

.footer-inner {
  max-width: 1120px;
  width: 100%;
  margin: 0 auto;
}

.footer-top {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  margin-bottom: 3rem;
  flex-wrap: wrap;
  gap: 2rem;
}

.footer-brand {
  display: flex;
  flex-direction: column;
  gap: 0.5rem;
}

.footer-logo {
  font-size: 1.5rem;
  font-weight: 700;
  letter-spacing: -0.03em;
}

.footer-tagline {
  font-size: 0.875rem;
  color: rgba(255, 255, 255, 0.5);
}

.footer-nav {
  display: flex;
  gap: 2rem;
}

.footer-nav a {
  color: rgba(255, 255, 255, 0.5);
  text-decoration: none;
  font-size: 0.875rem;
  transition: color var(--duration-normal) var(--ease-out);
}

.footer-nav a:hover {
  color: var(--bg);
}

.footer-divider {
  height: 1px;
  background: rgba(255, 255, 255, 0.1);
  margin-bottom: 2rem;
}

.footer-bottom {
  display: flex;
  justify-content: space-between;
  align-items: center;
  flex-wrap: wrap;
  gap: 1rem;
}

.footer-copy {
  font-size: 0.8125rem;
  color: rgba(255, 255, 255, 0.4);
}

.footer-built {
  font-family: var(--font-mono);
  font-size: 0.75rem;
  color: rgba(255, 255, 255, 0.3);
}

@media (max-width: 640px) {
  .footer-top {
    flex-direction: column;
  }

  .footer-nav {
    flex-wrap: wrap;
    gap: 1rem 1.5rem;
  }

  .footer-bottom {
    flex-direction: column;
    align-items: flex-start;
  }
}
</style>
