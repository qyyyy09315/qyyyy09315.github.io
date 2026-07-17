<template>
  <section class="footer animate fade-in">
    <div class="footer-inner">
      <div class="footer-left">
        <h2 class="footer-title">Yue-xin G.</h2>
        <p class="footer-tagline">大数据方向 · 本科在读</p>
      </div>

      <button class="footer-back" @click="goTo(0)">
        <svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M12 19V5M5 12l7-7 7 7"/></svg>
        返回顶部
      </button>
    </div>

    <div class="footer-bottom">
      <span class="footer-copyright">&copy; {{ currentYear }} Yue-xin G · 基于 Vue 3 + Vite</span>
      <div class="footer-links">
        <a href="https://github.com/qyyyy09315">GitHub</a>
        <a href="mailto:gengyuexin@qq.com">邮箱</a>
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
  display: flex;
  flex-direction: column;
  justify-content: center;
  padding: 4rem 2rem 2rem;
  background: #2a2520;
  color: #f7f4ed;
  position: relative;
}

.footer-inner {
  max-width: 1200px;
  width: 100%;
  margin: 0 auto;
  display: flex;
  align-items: flex-start;
  justify-content: space-between;
  padding-bottom: 2rem;
  border-bottom: 1px solid rgba(247, 244, 237, 0.1);
}

.footer-title {
  font-family: var(--font-sans);
  font-size: 2.5rem;
  font-weight: 700;
  letter-spacing: -.03em;
  margin-bottom: .5rem;
}

.footer-tagline {
  font-size: var(--text-base);
  color: rgba(247, 244, 237, 0.6);
}

.footer-back {
  font-family: var(--font-mono);
  font-size: var(--text-sm);
  color: rgba(247, 244, 237, 0.6);
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

.footer-bottom {
  max-width: 1200px;
  width: 100%;
  margin: 0 auto;
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding-top: 1.5rem;
}

.footer-copyright {
  font-size: var(--text-sm);
  color: rgba(247, 244, 237, 0.5);
}

.footer-links {
  display: flex;
  gap: 1.5rem;
}

.footer-links a {
  font-size: var(--text-sm);
  color: rgba(247, 244, 237, 0.5);
  text-decoration: none;
  transition: color var(--duration-fast) var(--ease-out);
}

.footer-links a:hover {
  color: var(--accent);
}

@media (max-width: 768px) {
  .footer { padding: 3rem 1.25rem 2rem; justify-content: flex-start; }

  .footer-inner {
    flex-direction: column;
    gap: 1.5rem;
    padding-bottom: 1.5rem;
  }

  .footer-bottom {
    flex-direction: column;
    gap: 1rem;
    align-items: flex-start;
  }
}
</style>
