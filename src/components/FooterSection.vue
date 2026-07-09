<template>
  <section class="footer">
    <div class="footer-inner">
      <div class="footer-top">
        <div class="footer-info">
          <h2 class="footer-title">Yue-xin G.</h2>
          <p class="footer-tagline">
            感谢阅读 · Thanks for scrolling
          </p>
        </div>

        <div class="footer-nav">
          <div class="footer-col">
            <h4 class="footer-nav-label">Pages</h4>
            <button class="footer-link" @click="goTo(0)">Home</button>
            <button class="footer-link" @click="goTo(1)">About</button>
            <button class="footer-link" @click="goTo(2)">Skills</button>
            <button class="footer-link" @click="goTo(3)">Education</button>
          </div>
          <div class="footer-col">
            <h4 class="footer-nav-label">Links</h4>
            <a class="footer-link" href="https://github.com/qyyyy09315">GitHub</a>
            <a class="footer-link" href="#">LinkedIn</a>
            <a class="footer-link" href="mailto:contact@example.com">Email</a>
          </div>
        </div>
      </div>

      <div class="footer-bottom">
        <span class="footer-copyright">&copy; {{ currentYear }} Yue-xin G. · Built with Vue 3 + Vite</span>
        <button class="footer-back" @click="goTo(0)">
          Back to Top
          <svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M12 19V5M5 12l7-7 7 7"/></svg>
        </button>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref, inject } from 'vue'

const currentYear = ref(new Date().getFullYear())
const goTo = inject('navigateTo', () => {})
</script>

<style scoped>
.footer {
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  padding: var(--space-24) var(--space-6);
  background: #0a0a0a;
  color: #fff;
}

.footer-inner {
  max-width: 1200px;
  width: 100%;
  margin: 0 auto;
}

.footer-top {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 4rem;
  padding-bottom: 4rem;
  border-bottom: 1px solid #333;
}

.footer-title {
  font-size: clamp(2.5rem, 5vw, 4rem);
  font-weight: 700;
  letter-spacing: -.03em;
  margin-bottom: 1rem;
}

.footer-tagline {
  font-size: var(--text-xl);
  color: #888;
}

.footer-nav {
  display: flex;
  gap: 4rem;
  justify-content: flex-end;
}

.footer-col {
  display: flex;
  flex-direction: column;
  gap: .75rem;
}

.footer-nav-label {
  font-family: var(--font-mono);
  font-size: var(--text-sm);
  text-transform: uppercase;
  letter-spacing: .1em;
  color: #666;
  margin-bottom: .5rem;
}

.footer-link {
  font-size: var(--text-lg);
  color: #ccc;
  text-decoration: none;
  background: none;
  border: none;
  cursor: pointer;
  text-align: left;
  padding: 0;
  transition: color var(--duration-fast) var(--ease-out);
}

.footer-link:hover {
  color: var(--accent);
}

.footer-bottom {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding-top: 2.5rem;
}

.footer-copyright {
  font-size: var(--text-base);
  color: #888;
}

.footer-back {
  font-family: var(--font-mono);
  font-size: var(--text-base);
  color: #ccc;
  background: none;
  border: none;
  cursor: pointer;
  display: inline-flex;
  align-items: center;
  gap: .5rem;
  transition: color var(--duration-fast) var(--ease-out);
}

.footer-back:hover {
  color: var(--accent);
}

@media (max-width: 768px) {
  .footer-top {
    grid-template-columns: 1fr;
    gap: 3rem;
  }
  .footer-nav { justify-content: flex-start; gap: 3rem; }
  .footer-bottom {
    flex-direction: column;
    gap: 1.5rem;
    align-items: flex-start;
  }
}
</style>