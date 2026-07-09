<template>
  <section class="hero">
    <div class="hero-inner">
      <div class="hero-content">
        <span class="hero-overline">Portfolio · 2024</span>
        <h1 class="hero-title">Yue-xin G.</h1>
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
            <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M7 17L17 7M17 7H7M17 7v10"/></svg>
          </button>
          <button class="btn btn-secondary" @click="navTo(2)">
            View Skills
          </button>
        </div>
      </div>

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

    <div class="scroll-hint">
      <span>Scroll</span>
      <div class="scroll-line"></div>
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
  padding: 6rem 2rem 4rem;
  position: relative;
}

.hero-inner {
  max-width: 1200px;
  width: 100%;
  margin: 0 auto;
  display: grid;
  grid-template-columns: 1.4fr 1fr;
  gap: 5rem;
  align-items: center;
}

.hero-overline {
  font-family: var(--font-mono);
  font-size: var(--text-sm);
  font-weight: 500;
  color: var(--text-muted);
  text-transform: uppercase;
  letter-spacing: .12em;
  margin-bottom: 2rem;
  display: block;
}

.hero-title {
  font-size: clamp(3.5rem, 7vw, 6rem);
  font-weight: 700;
  letter-spacing: -.04em;
  line-height: 1.05;
  margin-bottom: 2rem;
}

.hero-tagline {
  font-size: var(--text-xl);
  color: var(--text-secondary);
  line-height: 1.7;
  max-width: 520px;
  margin-bottom: 2.5rem;
}

.hero-meta {
  display: flex;
  gap: 2rem;
  margin-bottom: 3rem;
  flex-wrap: wrap;
}

.meta-item {
  display: flex;
  align-items: center;
  gap: .625rem;
  font-size: var(--text-base);
  color: var(--text-muted);
  font-family: var(--font-mono);
}

.meta-dot {
  width: 8px;
  height: 8px;
  border-radius: 50%;
  background: #22c55e;
  display: inline-block;
  box-shadow: 0 0 8px #22c55e66;
}

.hero-actions {
  display: flex;
  gap: 1.25rem;
  flex-wrap: wrap;
}

/* Right visual */
.hero-visual {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 2.5rem;
}

.avatar-frame {
  position: relative;
  width: 240px;
  height: 240px;
  border-radius: 24px;
  overflow: hidden;
  border: 1px solid var(--border);
}

.avatar-gradient {
  position: absolute;
  inset: 0;
  background: conic-gradient(
    from 0deg,
    #eff6ff, #dbeafe, #bfdbfe, #93c5fd,
    #60a5fa, #3b82f6, #2563eb, #1d4ed8,
    #1e40af, #1e3a8a, #172554, #eff6ff
  );
  animation: rotate 20s linear infinite;
}

@keyframes rotate { to { transform: rotate(360deg); } }

.avatar-content {
  position: absolute;
  inset: 4px;
  background: var(--bg);
  border-radius: 20px;
  display: flex;
  align-items: center;
  justify-content: center;
}

.avatar-mono {
  font-family: var(--font-mono);
  font-size: 3.5rem;
  color: var(--accent);
  font-weight: 600;
}

.hero-decor {
  display: flex;
  flex-direction: column;
  gap: 10px;
  align-items: center;
}

.decor-line {
  display: block;
  width: 1px;
  height: 56px;
  background: linear-gradient(to bottom, transparent, var(--border));
}

.decor-line.short {
  height: 36px;
  opacity: .6;
}

/* Scroll hint */
.scroll-hint {
  position: absolute;
  bottom: 2.5rem;
  left: 50%;
  transform: translateX(-50%);
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 10px;
}

.scroll-hint span {
  font-family: var(--font-mono);
  font-size: .75rem;
  text-transform: uppercase;
  letter-spacing: .12em;
  color: var(--text-muted);
  writing-mode: vertical-rl;
}

.scroll-line {
  width: 1px;
  height: 48px;
  background: linear-gradient(to bottom, var(--border), transparent);
  animation: scrollPulse 2s ease-in-out infinite;
}

@keyframes scrollPulse {
  0%, 100% { opacity: .4; transform: scaleY(.6); }
  50% { opacity: 1; transform: scaleY(1); }
}

@media (max-width: 768px) {
  .hero-inner {
    grid-template-columns: 1fr;
    text-align: center;
    gap: 3rem;
  }
  .hero-tagline { max-width: 100%; }
  .hero-meta { justify-content: center; }
  .hero-actions { justify-content: center; }
  .hero-visual { order: -1; }
  .avatar-frame { width: 160px; height: 160px; }
  .avatar-mono { font-size: 2.25rem; }
}
</style>