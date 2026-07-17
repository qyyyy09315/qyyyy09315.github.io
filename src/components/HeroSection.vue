<template>
  <section class="hero">
    <!-- Decorative blobs - positioned outside content flow -->
    <div class="decor-blob decor-blob--primary" style="width:420px;height:420px;top:-150px;left:-120px;"></div>
    <div class="decor-blob decor-blob--cyan" style="width:300px;height:300px;top:25%;right:-80px;"></div>
    <div class="decor-blob decor-blob--accent" style="width:200px;height:200px;bottom:-60px;left:30%;"></div>
    <div class="decor-grid"></div>

    <div class="hero-inner">
      <!-- Left content with stagger -->
      <div class="hero-content">
        <span class="hero-overline animate fade-up" style="--delay: 0.15s">个人主页 · 2023 级</span>
        <h1 class="hero-title animate fade-up" style="--delay: 0.3s">Yue-xin G.</h1>
        <p class="hero-tagline animate fade-up" style="--delay: 0.45s">
          数据科学与大数据技术 · 本科在读<br>
          专注于 <span class="text-accent">机器学习</span><span class="punct">，</span><span class="text-accent">交叉科学</span><span class="punct">，</span><span class="text-accent">自动化技术</span>
        </p>
        <div class="hero-meta animate fade-up" style="--delay: 0.6s">
          <span class="meta-item"><span class="meta-dot"></span>辽宁大连</span>
          <span class="meta-item"><span class="meta-dot"></span>数据科学与大数据技术</span>
        </div>
        <p class="hero-objective animate fade-up" style="--delay: 0.75s">
          扎实的 Python / SQL 编程能力，对数据建模、统计分析和可视化有系统实践。寻求数据科学、机器学习方向实习与工作机会。
        </p>
        <blockquote class="hero-quote animate fade-up" style="--delay: 0.9s">
          <span class="quote-zh">步履轻踏破浩瀚，铁拳微舒碎苍寰</span>
          <span class="quote-en">Particle or planet — it all shatters with enough force.</span>
        </blockquote>
        <div class="hero-actions animate fade-up" style="--delay: 1.05s">
          <button class="btn btn-primary" @click="navTo(5)">
            <span>联系我</span>
            <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M7 17L17 7M17 7H7M17 7v10"/></svg>
          </button>
          <button class="btn btn-secondary" @click="navTo(2)">查看技能</button>
        </div>
      </div>

      <!-- Right visual with scale-in -->
      <div class="hero-visual animate scale-in" style="--delay: 0.5s">
        <div class="photo-frame">
          <img src="../assets/avatar.jpg" alt="Yue-xin G. 证件照" class="photo-img" loading="lazy" decoding="async" />
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

    <div class="section-divider"></div>
  </section>
</template>

<script setup>
import { inject } from 'vue'
const navTo = inject('navigateTo', () => {})
</script>

<style scoped>
.hero {
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  padding: 6rem 2rem 3rem;
  position: relative;
}

.hero-inner {
  max-width: 1200px;
  width: 100%;
  margin: 0 auto;
  display: grid;
  grid-template-columns: 1.3fr 1fr;
  gap: 5rem;
  align-items: start;
  padding-top: 1rem;
  position: relative;
  z-index: 1;
}

.hero-overline {
  font-family: var(--font-mono);
  font-size: var(--text-sm);
  font-weight: 500;
  color: var(--text-muted);
  text-transform: uppercase;
  letter-spacing: .1em;
  margin-bottom: 1rem;
  display: block;
}

.hero-title {
  font-family: 'Caveat', 'Kalam', 'Brush Script MT', cursive;
  font-size: clamp(3.5rem, 8vw, 6rem);
  font-weight: 600;
  letter-spacing: -.02em;
  line-height: 1.05;
  margin-bottom: 1.25rem;
  color: var(--text);
}

.hero-tagline {
  font-size: var(--text-lg);
  color: var(--text-secondary);
  line-height: 1.7;
  margin-bottom: 1.25rem;
}

.text-accent {
  color: var(--accent);
  font-weight: 500;
}

.hero-meta {
  display: flex;
  gap: 1.25rem;
  margin-bottom: 1.25rem;
  flex-wrap: wrap;
}

.meta-item {
  display: flex;
  align-items: center;
  gap: .5rem;
  font-size: var(--text-sm);
  color: var(--text-secondary);
}

.meta-dot {
  width: 8px;
  height: 8px;
  border-radius: 50%;
  background: var(--accent-mint);
  display: inline-block;
  flex-shrink: 0;
}

.hero-objective {
  font-size: var(--text-base);
  color: var(--text-secondary);
  line-height: 1.7;
  margin-bottom: 1.25rem;
  padding: .875rem 1.125rem;
  background: var(--accent-subtle);
  border-radius: 8px;
}

.hero-quote {
  font-size: var(--text-base);
  color: var(--text-secondary);
  line-height: 1.7;
  margin-bottom: 1.5rem;
  padding: 1rem 1.25rem;
  background: var(--bg-subtle);
  border-radius: 10px;
  text-align: center;
}

.quote-zh {
  font-size: 1.25rem;
  font-weight: 500;
  line-height: 1.6;
  display: block;
  text-align: center;
}

.quote-en {
  font-family: var(--font-mono);
  font-size: var(--text-sm);
  color: var(--text-muted);
  display: block;
  margin-top: .375rem;
  letter-spacing: .02em;
  white-space: nowrap;
  text-align: center;
}

.hero-actions {
  display: flex;
  gap: .75rem;
  flex-wrap: wrap;
}

.hero-visual {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 1.75rem;
}

.photo-frame {
  position: relative;
  width: 260px;
  height: 340px;
  border-radius: 20px;
  overflow: hidden;
  border: 2px solid var(--accent-muted);
  box-shadow: 0 12px 48px -12px var(--accent-shadow), 0 4px 16px rgba(0,0,0,.06);
}

.photo-img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  display: block;
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

.scroll-hint {
  position: absolute;
  bottom: 2rem;
  left: 50%;
  transform: translateX(-50%);
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 8px;
  z-index: 1;
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

/* Pure CSS animation - smooth & natural */
.animate {
  opacity: 0;
  animation-fill-mode: both;
  animation-duration: 0.8s;
  animation-timing-function: cubic-bezier(0.22, 1, 0.36, 1);
  animation-delay: var(--delay, 0s);
}


.animate.visible {
  animation-name: fadeUp;
}

.fade-up.visible {
  animation-name: fadeUp;
}

.scale-in.visible {
  animation-name: scaleIn;
}

@keyframes fadeUp {
  from {
    opacity: 0;
    transform: translateY(32px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

@keyframes scaleIn {
  from {
    opacity: 0;
    transform: scale(0.95);
  }
  to {
    opacity: 1;
    transform: scale(1);
  }
}

@media (max-width: 768px) {
  .hero {
    padding: 4.5rem 1.25rem 2rem;
    justify-content: flex-start;
  }

  .hero-inner {
    grid-template-columns: 1fr;
    text-align: center;
    gap: 1.75rem;
  }

  .hero-title {
    font-size: clamp(2.75rem, 11vw, 4.5rem);
  }

  .hero-tagline { font-size: var(--text-base); }

  .hero-meta {
    justify-content: center;
    gap: .875rem;
    margin-bottom: 1rem;
  }

  .hero-objective {
    text-align: left;
    font-size: var(--text-sm);
    padding: .75rem 1rem;
  }

  .hero-quote {
    text-align: left;
    font-size: var(--text-sm);
    padding: .875rem 1rem;
    margin-bottom: 1.25rem;
  }

  .hero-actions { justify-content: center; }
  .hero-visual { order: -1; }

  .photo-frame {
    width: 180px;
    height: 240px;
    border-radius: 16px;
  }

  .decor-line { height: 36px; }
  .decor-line.short { height: 24px; }

  .scroll-hint { display: none; }

  .decor-blob {
    filter: blur(50px);
    opacity: 0.25;
  }

  .decor-blob--primary {
    width: 220px !important;
    height: 220px !important;
    top: -80px !important;
    left: -60px !important;
  }

  .decor-blob--cyan {
    width: 160px !important;
    height: 160px !important;
    right: -40px !important;
  }

  .decor-blob--accent {
    width: 120px !important;
    height: 120px !important;
  }
}
</style>
