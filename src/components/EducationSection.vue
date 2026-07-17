<template>
  <section class="section" id="education">
    <div class="decor-blob decor-blob--cyan" style="width:320px;height:320px;bottom:-100px;left:-90px;"></div>
    <div class="decor-blob decor-blob--green" style="width:200px;height:200px;top:-60px;right:-60px;"></div>
    <div class="decor-shape decor-shape--cross" style="top:55%;right:12%;"></div>
    <div class="decor-shape decor-shape--dot" style="top:20%;left:18%;"></div>

    <div class="content" style="position:relative;z-index:1;">
      <div
        class="section-header"
        v-motion
        :initial="{ opacity: 0, y: 30 }"
        :visible-once="{ opacity: 1, y: 0, transition: { duration: 500, ease: 'easeOut' } }"
      >
        <h2 class="section-title">教育与荣誉</h2>
      </div>

      <div class="edu-timeline">
        <div class="edu-card">
          <div class="edu-year">2023 — 2027</div>
          <h3 class="edu-school">大连海洋大学</h3>
          <p class="edu-major">数据科学与大数据技术 · 本科在读</p>
        </div>

        <div class="edu-card">
          <div class="edu-year">2020 — 2023</div>
          <h3 class="edu-school">大连市第二十三高级中学</h3>
          <p class="edu-major">高中</p>
        </div>
      </div>

      <div class="awards-block">
        <div class="award-item" v-motion :initial="{ opacity: 0, scale: 0.9 }" :visible-once="{ opacity: 1, scale: 1, transition: { delay: 200, duration: 400, ease: 'easeOut' } }">
          <div class="award-icon">
            <svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><circle cx="12" cy="8" r="7"/><polyline points="8.21 13.89 7 23 12 20 17 23 15.79 13.88"/></svg>
          </div>
          <div class="award-content">
            <span class="award-name">大连海洋大学科技创新先进个人</span>
            <span class="award-period">2024 — 2026 两年度</span>
          </div>
        </div>
      </div>
    </div>

    <div class="section-divider"></div>
  </section>
</template>

<style scoped>
.section {
  display: flex;
  flex-direction: column;
  justify-content: center;
  padding: 4rem 2rem;
  position: relative;
}

.content {
  max-width: 900px;
  width: 100%;
  margin: 0 auto;
}

.section-header {
  margin-bottom: 2rem;
}

.section-title {
  font-size: clamp(1.5rem, 3.5vw, 2rem);
  font-weight: 600;
  letter-spacing: -.02em;
  line-height: 1.2;
}

.edu-timeline {
  display: flex;
  flex-direction: column;
  gap: 1rem;
  margin-bottom: 2rem;
  position: relative;
}

.edu-card {
  display: grid;
  grid-template-columns: 180px 1fr;
  gap: 1.5rem;
  align-items: center;
  padding: 1.25rem;
  background: var(--bg-subtle);
  border-radius: 10px;
}

.edu-year {
  font-family: var(--font-mono);
  font-size: var(--text-sm);
  font-weight: 600;
  color: var(--accent);
  letter-spacing: -.02em;
}

.edu-school {
  font-size: var(--text-lg);
  font-weight: 600;
  margin-bottom: .25rem;
}

.edu-major {
  font-size: var(--text-base);
  color: var(--text-secondary);
}

.awards-block {
  margin-top: 2rem;
}

.award-item {
  display: flex;
  align-items: center;
  gap: 1rem;
  padding: 1.25rem 1.5rem;
  background: var(--award-gradient);
  border: 1px solid var(--award-border);
  border-radius: 10px;
}

.award-icon {
  color: var(--award-icon);
  flex-shrink: 0;
}

.award-content {
  display: flex;
  flex-direction: column;
  gap: .25rem;
}

.award-name {
  font-size: var(--text-base);
  font-weight: 600;
  color: var(--award-text);
}

.award-period {
  font-family: var(--font-mono);
  font-size: var(--text-sm);
  color: var(--award-icon);
}

@media (max-width: 768px) {
  .section { padding: 3rem 1.25rem; justify-content: flex-start; }

  .edu-card {
    grid-template-columns: 1fr;
    gap: .5rem;
    padding: 1rem;
  }

  .award-item {
    padding: 1rem;
  }

  .decor-blob { opacity: 0.25; }
}
</style>
