<template>
  <section class="hero">
    <div class="hero-inner">
      <!-- Left: Text content -->
      <div class="hero-content">
        <span class="hero-overline">Portfolio · 2024</span>
        <h1 class="hero-title">
          Yue-xin G.
        </h1>
        <p class="hero-tagline">
          Big Data student &amp; aspiring data scientist exploring
          the intersection of machine learning, statistics, and software.
        </p>
        <div class="hero-meta">
          <span class="meta-item">
            <span class="meta-dot"></span>
            Dalian, China
          </span>
          <span class="meta-item">
            <span class="meta-dot"></span>
            Big Data Science
          </span>
        </div>
        <div class="hero-actions">
          <button class="btn btn-primary" @click="navTo(4)">
            <span>Get in Touch</span>
            <svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M7 17L17 7M17 7H7M17 7v10"/></svg>
          </button>
          <button class="btn btn-secondary" @click="navTo(2)">
            View Skills
          </button>
        </div>
      </div>

      <!-- Right: Visual element -->
      <div class="hero-visual">
        <div class="avatar-frame">
          <div class="avatar-gradient"></div>
          <div class="avatar-content">
            <span class="avatar-mono">&lt;/&gt;</span>
          </div>
        </div>
        <div class="hero-decor">
          <span class="decor-line"></span>
          <span class="decor-line short"></span>
        </div>
      </div>
    </div>

    <!-- Scroll hint -->
    <div class="scroll-hint">
      <span>Scroll</span>
      <div class="scroll-line"></div>
    </div>
  </section>
</template>

<script setup>
import { inject, onMounted, ref } from 'vue'

const navTo = inject('navigateTo', () => {})
const isVisible = ref(false)

onMounted(() => {
  isVisible.value = true
})
</script>

<style scoped>
.hero {
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  padding: 5rem 2rem 3rem;
  position: relative;
  overflow: hidden;
}

.hero-inner {
  max-width: 1120px;
  width: 100%;
  margin: 0 auto;
  display: grid;
  grid-template-columns: 1.4fr 1fr;
  gap: 4rem;
  align-items: center;
}

.hero-overline {
  font-family: var(--font-mono);
  font-size: 0.75rem;
  font-weight: 500;
  color: var(--text-muted);
  text-transform: uppercase;
  letter-spacing: 0.1em;
  margin-bottom: 1.5rem;
  display: block;
}

.hero-title {
  font-size: clamp(2.75rem, 5.5vw, 4.5rem);
  font-weight: 700;
  letter-spacing: -0.04em;
  line-height: 1.05;
  margin-bottom: 1.5rem;
}

.hero-tagline {
  font-size: 1.125rem;
  color: var(--text-secondary);
  line-height: 1.7;
  max-width: 480px;
  margin-bottom: 2rem;
}

.hero-meta {
  display: flex;
  gap: 1.5rem;
  margin-bottom: 2.5rem;
  flex-wrap: wrap;
}

.meta-item {
  display: flex;
  align-items: center;
  gap: 0.5rem;
  font-size: 0.875rem;
  color: var(--text-muted);
  font-family: var(--font-mono);
}

.meta-dot {
  width: 6px;
  height: 6px;
  border-radius: 50%;
  background: #22c55e;
  display: inline-block;
}

.hero-actions {
  display: flex;
  gap: 1rem;
  flex-wrap: wrap;
}

/* Right side visual */
.hero-visual {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 2rem;
}

.avatar-frame {
  position: relative;
  width: 200px;
  height: 200px;
  border-radius: 20px;
  overflow: hidden;
  border: 1px solid var(--border);
}

.avatar-gradient {
  position: absolute;
  inset: 0;
  background: conic-gradient(
    from 0deg,
    #eff6ff,
    #dbeafe,
    #bfdbfe,
    #93c5fd,
    #60a5fa,
    #3b82f6,
    #2563eb,
    #1d4ed8,
    #1e40af,
    #1e3a8a,
    #172554,
    #eff6ff
  );
  animation: rotate 20s linear infinite;
}

@keyframes rotate {
  to { transform: rotate(360deg); }
}

.avatar-content {
  position: absolute;
  inset: 3px;
  background: var(--bg);
  border-radius: 17px;
  display: flex;
  align-items: center;
  justify-content: center;
}

.avatar-mono {
  font-family: var(--font-mono);
  font-size: 3rem;
  color: var(--accent);
  font-weight: 500;
}

.hero-decor {
  display: flex;
  flex-direction: column;
  gap: 8px;
  align-items: center;
}

.decor-line {
  display: block;
  width: 1px;
  height: 48px;
  background: linear-gradient(to bottom, transparent, var(--border));
}

.decor-line.short {
  height: 32px;
  opacity: 0.6;
}

/* Scroll hint */
.scroll-hint {
  position: absolute;
  bottom: 2rem;
  left: 50%;
  transform: translateX(-50%);
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 8px;
}

.scroll-hint span {
  font-family: var(--font-mono);
  font-size: 0.6875rem;
  text-transform: uppercase;
  letter-spacing: 0.1em;
  color: var(--text-muted);
  writing-mode: vertical-rl;
  text-orientation: mixed;
}

.scroll-line {
  width: 1px;
  height: 40px;
  background: linear-gradient(to bottom, var(--border), transparent);
  animation: scrollPulse 2s ease-in-out infinite;
}

@keyframes scrollPulse {
  0%, 100% { opacity: 0.4; transform: scaleY(0.6); }
  50% { opacity: 1; transform: scaleY(1); }
}

/* Responsive */
@media (max-width: 768px) {
  .hero-inner {
    grid-template-columns: 1fr;
    text-align: center;
    gap: 3rem;
  }

  .hero-tagline {
    max-width: 100%;
  }

  .hero-meta {
    justify-content: center;
  }

  .hero-actions {
    justify-content: center;
  }

  .hero-visual {
    order: -1;
  }

  .avatar-frame {
    width: 140px;
    height: 140px;
  }

  .avatar-mono {
    font-size: 2rem;
  }
}

@media (max-width: 480px) {
  .hero {
    padding: 4rem 1.5rem 2rem;
  }
}
</style>
