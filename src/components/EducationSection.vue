<template>
  <section id="education" class="section">
    <div class="content">
      <div class="section-header">
        <div class="animate"><span class="section-label">03 / 教育</span></div>
        <h2 class="section-title animate animate-delay-1">教育背景</h2>
        <p class="section-subtitle animate animate-delay-2">
          学习经历
        </p>
      </div>

      <div class="edu-timeline">
        <div class="edu-card card animate animate-delay-2">
          <div class="edu-year">2023 — 2027</div>
          <h3 class="edu-school">大连海洋大学</h3>
          <p class="edu-major">数据科学与大数据技术 · 本科在读</p>
        </div>

        <div class="edu-card card animate animate-delay-3">
          <div class="edu-year">2020 — 2023</div>
          <h3 class="edu-school">大连市第二十三高级中学</h3>
          <p class="edu-major">高中</p>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.section {
  display: flex;
  flex-direction: column;
  justify-content: center;
  padding: 5rem 2rem;
}

.content {
  max-width: 1200px;
  width: 100%;
  margin: 0 auto;
}

.section-header {
  margin-bottom: 2.5rem;
}

.section-label {
  font-family: var(--font-mono);
  font-size: var(--text-sm);
  font-weight: 500;
  color: var(--accent);
  text-transform: uppercase;
  letter-spacing: .08em;
  margin-bottom: .5rem;
  display: block;
}

.section-title {
  font-size: clamp(1.75rem, 4vw, 2.5rem);
  font-weight: 700;
  letter-spacing: -.03em;
  line-height: 1.15;
}

.section-subtitle {
  color: var(--text-secondary);
  margin-top: .5rem;
  font-size: var(--text-lg);
  font-weight: 400;
}

.edu-timeline {
  display: flex;
  flex-direction: column;
  gap: 1rem;
}

.edu-card {
  display: grid;
  grid-template-columns: 180px 1fr;
  gap: 1.5rem;
  align-items: center;
  padding: 1.5rem;
}

.edu-year {
  font-family: var(--font-mono);
  font-size: var(--text-lg);
  font-weight: 600;
  color: var(--accent);
  letter-spacing: -.02em;
}

.edu-school {
  font-size: var(--text-xl);
  font-weight: 700;
  margin-bottom: .25rem;
}

.edu-major {
  font-size: var(--text-base);
  color: var(--text-secondary);
}

@media (max-width: 768px) {
  .section {
    padding: 4rem 1.25rem 3rem;
    justify-content: flex-start;
  }

  .edu-card {
    grid-template-columns: 1fr;
    gap: .5rem;
    padding: 1rem;
  }

  .edu-school {
    font-size: var(--text-lg);
  }
}
</style>