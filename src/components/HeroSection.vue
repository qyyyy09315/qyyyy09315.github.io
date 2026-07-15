<template>
  <section class="hero">
    <div class="hero-inner">
      <div class="hero-content">
        <span class="hero-overline">个人主页 · 2023</span>
        <h1 class="hero-title">Yue-xin G.</h1>

        <!-- Career Objective -->
        <div class="hero-objective">
          大数据专业方向，专注机器学习与数据工程交叉领域。扎实的 Python / SQL 编程能力，对数据建模、统计分析和可视化有系统实践经验。寻求数据科学、机器学习方向的实习与工作机会。
        </div>

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
        <p class="hero-quote">
          步履轻踏破浩瀚，铁拳微舒碎苍寰<br>
          <span class="quote-en">Particle or planet, it all shatters with enough force.</span>
        </p>
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
          <img src="../assets/avatar.jpg" alt="Yue-xin G. 证件照" class="avatar-img" />
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
  font-family: 'Caveat', 'Brush Script MT', cursive;
  font-size: clamp(4rem, 9vw, 7rem);
  font-weight: 600;
  letter-spacing: -.02em;
  line-height: 1.1;
  margin-bottom: 1.5rem;
  background: linear-gradient(135deg, var(--accent) 0%, #6366f1 50%, #8b5cf6 100%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}

/* Career Objective */
.hero-objective {
  font-size: var(--text-base);
  color: var(--text-secondary);
  line-height: 1.7;
  max-width: 500px;
  margin-bottom: 1.5rem;
  padding: 1rem 1.25rem;
  background: var(--accent-subtle);
  border-radius: 8px;
  border-left: 3px solid var(--accent);
}

/* Quote */
.hero-quote {
  font-size: var(--text-lg);
  color: var(--text-secondary);
  line-height: 1.8;
  margin-bottom: 2.5rem;
  padding: 1.5rem 2rem;
  background: var(--bg-subtle);
  border-radius: 12px;
  border-left: 4px solid var(--accent);
  max-width: 520px;
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

.quote-en {
  font-family: var(--font-mono);
  font-size: var(--text-sm);
  color: var(--text-muted);
  display: block;
  margin-top: .5rem;
  letter-spacing: .02em;
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
  border-radius: 50%;
  overflow: hidden;
  border: 3px solid var(--accent-muted);
  box-shadow: 0 0 32px rgba(37, 99, 235, .15);
}

.avatar-img {
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

@media (max-width: 768px) {
  .hero {
    padding: 5rem 1.25rem 2rem;
    justify-content: flex-start;
  }

  .hero-inner {
    grid-template-columns: 1fr;
    text-align: center;
    gap: 2rem;
  }

  .hero-title {
    font-size: clamp(3rem, 12vw, 5rem);
  }

  .hero-tagline {
    max-width: 100%;
    font-size: var(--text-base);
  }

  .hero-objective {
    max-width: 100%;
    text-align: left;
  }

  .hero-quote {
    text-align: left;
    padding: 1rem 1.25rem;
    font-size: var(--text-base);
  }

  .hero-meta {
    justify-content: center;
    gap: 1rem;
    margin-bottom: 1.5rem;
  }

  .hero-actions {
    justify-content: center;
  }

  .hero-visual {
    order: -1;
  }

  .avatar-frame {
    width: 130px;
    height: 130px;
  }

  .scroll-hint {
    display: none;
  }
}
</style>
