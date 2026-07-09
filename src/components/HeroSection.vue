<template>
  <section class="hero">
    <div class="hero-inner">
      <div class="hero-content">
        <span class="hero-overline">个人主页 · 2024</span>
        <h1 class="hero-title">岳馨</h1>
        <p class="hero-tagline">
          大数据专业学生 · 数据科学方向学习者<br>
          专注于机器学习、统计分析与软件工程的交叉领域
        </p>
        <div class="hero-meta">
          <span class="meta-item">
            <span class="meta-dot"></span>
            辽宁大连
          </span>
          <span class="meta-item">
            <span class="meta-dot"></span>
            数据科学与大数据技术
          </span>
        </div>
        <div class="hero-actions">
          <button class="btn btn-primary" @click="navTo(4)">
            <span>联系我</span>
            <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M7 17L17 7M17 7H7M17 7v10"/></svg>
          </button>
          <button class="btn btn-secondary" @click="navTo(2)">
            查看技能
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
      <span>滑动</span>
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
  padding: 5rem 2rem 3rem;
  position: relative;
}

.hero-inner {
  max-width: 1200px;
  width: 100%;
  margin: 0 auto;
  display: grid;
  grid-template-columns: 1.2fr 1fr;
  gap: 5rem;
  align-items: center;
}

.hero-overline {
  font-family: var(--font-mono);
  font-size: 0.8125rem;
  font-weight: 500;
  color: var(--text-muted);
  text-transform: uppercase;
  letter-spacing: .1em;
  margin-bottom: 1.5rem;
  display: block;
}

.hero-title {
  font-size: clamp(4rem, 9vw, 7rem);
  font-weight: 700;
  letter-spacing: -.03em;
  line-height: 1.05;
  margin-bottom: 1.5rem;
}

.hero-tagline {
  font-size: 1.25rem;
  color: var(--text-secondary);
  line-height: 1.8;
  max-width: 500px;
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
  gap: .5rem;
  font-size: .9375rem;
  color: var(--text-secondary);
}

.meta-dot {
  width: 8px;
  height: 8px;
  border-radius: 50%;
  background: #22c55e;
  display: inline-block;
  box-shadow: 0 0 6px rgba(34, 197, 94, .5);
}

.hero-actions {
  display: flex;
  gap: 1rem;
  flex-wrap: wrap;
}

/* Right visual */
.hero-visual {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 2rem;
}

.avatar-frame {
  position: relative;
  width: 220px;
  height: 220px;
  border-radius: 24px;
  overflow: hidden;
  border: 1px solid var(--border);
}

.avatar-gradient {
  position: absolute;
  inset: 0;
  background: conic-gradient(from 0deg, #eff6ff, #dbeafe, #bfdbfe, #93c5fd, #60a5fa, #3b82f6, #2563eb, #1d4ed8, #1e40af, #1e3a8a, #172554, #eff6ff);
  animation: rotate 20s linear infinite;
}

@keyframes rotate {
  to { transform: rotate(360deg); }
}

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
  opacity: .6;
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
  font-size: .6875rem;
  text-transform: uppercase;
  letter-spacing: .1em;
  color: var(--text-muted);
  writing-mode: vertical-rl;
}

.scroll-line {
  width: 1px;
  height: 40px;
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
    gap: 2.5rem;
  }
  .hero-tagline { max-width: 100%; }
  .hero-meta { justify-content: center; }
  .hero-actions { justify-content: center; }
  .hero-visual { order: -1; }
  .avatar-frame { width: 150px; height: 150px; }
  .avatar-mono { font-size: 2.25rem; }
}
</style>