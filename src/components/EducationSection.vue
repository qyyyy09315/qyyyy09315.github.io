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
.edu-timeline {
  display: flex;
  flex-direction: column;
  gap: 1.5rem;
}

.edu-card {
  display: grid;
  grid-template-columns: 200px 1fr;
  gap: 1.5rem;
  align-items: center;
  padding: var(--space-8);
}

.edu-year {
  font-family: var(--font-mono);
  font-size: var(--text-lg);
  font-weight: 600;
  color: var(--accent);
  letter-spacing: -.02em;
}

.edu-school {
  font-size: var(--text-2xl);
  font-weight: 700;
  margin-bottom: .25rem;
}

.edu-major {
  font-size: var(--text-lg);
  color: var(--text-secondary);
}

@media (max-width: 768px) {
  .edu-card {
    grid-template-columns: 1fr;
    gap: .5rem;
  }
}
</style>