<template>
  <section class="hero">
    <div class="content">
      <span class="hero-label">Hello, World</span>
      <h1>I'm Yue-xin G.</h1>
      <p class="hero-subtitle">
        大数据专业学生 · 对机器学习和数据科学充满热情<br>
        Passionate about Machine Learning &amp; Data Science
      </p>
      <div class="hero-actions">
        <button class="btn btn-primary" @click="navTo(4)">
          Get in Touch
        </button>
        <button class="btn btn-secondary" @click="navTo(2)">
          View Skills
        </button>
      </div>
    </div>
  </section>
</template>

<script setup>
import { inject } from 'vue'

const navTo = inject('navigateTo', () => {})
</script>

<style scoped>
.hero {
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  padding: 6rem 0;
}

.content {
  max-width: 960px;
  width: 100%;
  padding: 0 2rem;
}

.hero-label {
  font-size: 0.875rem;
  color: #2563eb;
  font-weight: 500;
  margin-bottom: 1rem;
  letter-spacing: 0.05em;
}

.hero h1 {
  font-size: clamp(2.5rem, 6vw, 4rem);
  font-weight: 600;
  letter-spacing: -0.03em;
  line-height: 1.1;
  margin-bottom: 1.5rem;
}

.hero-subtitle {
  font-size: 1.25rem;
  color: #6b7280;
  font-weight: 300;
  line-height: 1.8;
  margin-bottom: 2.5rem;
}

.hero-actions {
  display: flex;
  gap: 1rem;
  flex-wrap: wrap;
}

.btn {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  padding: 0.75rem 1.5rem;
  border-radius: 8px;
  font-size: 0.875rem;
  font-weight: 500;
  text-decoration: none;
  transition: all 0.2s;
  cursor: pointer;
  border: none;
}

.btn-primary {
  background: #2563eb;
  color: white;
}

.btn-primary:hover {
  background: #1d4ed8;
  transform: translateY(-1px);
}

.btn-secondary {
  background: #f9fafb;
  color: #1a1a1a;
  border: 1px solid #e5e7eb;
}

.btn-secondary:hover {
  border-color: #2563eb;
  color: #2563eb;
}

@media (max-width: 640px) {
  .hero {
    min-height: 100vh;
    padding: 5rem 0 3rem;
  }
}
</style>