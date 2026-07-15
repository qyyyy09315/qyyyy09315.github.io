<template>
  <section class="hero">
    <div class="hero-inner">
      <!-- 左侧文字 -->
      <div class="hero-content">
        <span class="hero-overline">个人主页 · 2023 级</span>
        <h1 class="hero-title">Yue-xin G.</h1>
        <p class="hero-tagline">
          数据科学与大数据技术 · 本科在读<br>
          专注机器学习 × 数据工程 × 可视化
        </p>

        <div class="hero-meta">
          <span class="meta-item"><span class="meta-dot"></span>辽宁大连</span>
          <span class="meta-item"><span class="meta-dot"></span>数据科学与大数据技术</span>
        </div>

        <p class="hero-objective">
          扎实的 Python / SQL 编程能力，对数据建模、统计分析和可视化有系统实践。寻求数据科学、机器学习方向实习与工作机会。
        </p>

        <blockquote class="hero-quote">
          步履轻踏破浩瀚，铁拳微舒碎苍寰
          <span class="quote-en">Particle or planet — it all shatters with enough force.</span>
        </blockquote>

        <div class="hero-actions">
          <button class="btn btn-primary" @click="navTo(5)">
            <span>联系我</span>
            <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M7 17L17 7M17 7H7M17 7v10"/></svg>
          </button>
          <button class="btn btn-secondary" @click="navTo(2)">
            查看技能
          </button>
        </div>
      </div>

      <!-- 右侧照片 -->
      <div class="hero-visual">
        <div class="photo-frame">
          <img src="../assets/avatar.jpg" alt="Yue-xin G. 证件照" class="photo-img" />
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
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  padding: 5rem 2rem 3rem;
  position: relative;
}

.hero-inner {
  max-width: 1200px;
  width: 100%;
  margin: 0 auto;
  display: grid;
  grid-template-columns: 1.3fr 1fr;
  gap: 4rem;
  align-items: start;
  padding-top: 1rem;
}

/* ---- Left content ---- */

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
  background: #22c55e;
  display: inline-block;
  box-shadow: 0 0 6px rgba(34, 197, 94, .5);
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

/* Quote */
.hero-quote {
  font-size: var(--text-base);
  color: var(--text-secondary);
  line-height: 1.7;
  margin-bottom: 1.5rem;
  padding: 1rem 1.25rem;
  background: var(--bg-subtle);
  border-radius: 10px;
}

.quote-en {
  font-family: var(--font-mono);
  font-size: var(--text-sm);
  color: var(--text-muted);
  display: block;
  margin-top: .375rem;
  letter-spacing: .02em;
}

.hero-actions {
  display: flex;
  gap: .75rem;
  flex-wrap: wrap;
}

/* ---- Right visual — rectangular photo ---- */

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
  box-shadow: 0 8px 40px rgba(37, 99, 235, .12), 0 2px 12px rgba(0,0,0,.06);
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

/* ---- Mobile ---- */

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

  .hero-tagline {
    font-size: var(--text-base);
  }

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

  .hero-actions {
    justify-content: center;
  }

  .hero-visual {
    order: -1;
  }

  .photo-frame {
    width: 180px;
    height: 240px;
    border-radius: 16px;
  }

  .decor-line { height: 36px; }
  .decor-line.short { height: 24px; }

  .scroll-hint { display: none; }
}
</style>
