<template>
  <section id="footer" class="section">
    <div class="content">
      <div class="footer-inner">
        <p class="footer-logo">Yue-xin G.</p>
        <p class="footer-text">&copy; {{ currentYear }} Yue-xin G. All rights reserved.</p>
        <div class="footer-links">
          <a href="https://github.com/qyyyy09315" target="_blank">GitHub</a>
          <span class="divider">·</span>
          <a href="#hero" @click.prevent="goTo(0)">返回顶部</a>
        </div>
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
.section {
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  background: #f9fafb;
}

.content {
  max-width: 960px;
  width: 100%;
  margin: 0 auto;
  padding: 0 2rem;
}

.footer-inner {
  text-align: center;
}

.footer-logo {
  font-size: 1.25rem;
  font-weight: 600;
  letter-spacing: -0.02em;
  margin-bottom: 1rem;
}

.footer-text {
  font-size: 0.875rem;
  color: #6b7280;
  margin-bottom: 1.5rem;
}

.footer-links {
  font-size: 0.875rem;
  color: #6b7280;
}

.footer-links a {
  color: #2563eb;
  text-decoration: none;
}

.footer-links a:hover {
  text-decoration: underline;
}

.divider {
  margin: 0 0.5rem;
  color: #d1d5db;
}
</style>