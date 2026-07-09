<template>
  <section id="about" class="section">
    <div class="content">
      <div class="section-header">
        <div class="animate"><span class="section-label">01 / About</span></div>
        <h2 class="section-title animate animate-delay-1">About Me</h2>
        <p class="section-subtitle animate animate-delay-2">
          关于我
        </p>
      </div>

      <div class="about-grid">
        <div class="card about-card animate animate-delay-2">
          <div class="card-icon">
            <svg width="22" height="22" fill="none" stroke="currentColor" stroke-width="2"><circle cx="12" cy="8" r="4"/><path d="M4 20c0-4 4-7 8-7s8 3 8 7"/></svg>
          </div>
          <div class="card-text">
            <span class="meta">Name</span>
            <span class="value">Yue-xin G.</span>
          </div>
        </div>

        <div class="card about-card animate animate-delay-3">
          <div class="card-icon">
            <svg width="22" height="22" fill="none" stroke="currentColor" stroke-width="2"><path d="M12 2v20M2 12h20"/></svg>
          </div>
          <div class="card-text">
            <span class="meta">Location</span>
            <span class="value">Dalian, China</span>
          </div>
        </div>

        <div class="card about-card animate animate-delay-4">
          <div class="card-icon">
            <svg width="22" height="22" fill="none" stroke="currentColor" stroke-width="2"><rect x="3" y="4" width="18" height="16" rx="2"/><path d="M16 2v4M8 2v4M3 10h18"/></svg>
          </div>
          <div class="card-text">
            <span class="meta">Major</span>
            <span class="value">Big Data Science</span>
          </div>
        </div>

        <div class="card about-card animate animate-delay-5">
          <div class="card-icon">
            <svg width="22" height="22" fill="none" stroke="currentColor" stroke-width="2"><circle cx="12" cy="12" r="10"/><path d="M12 6v6l4 2"/></svg>
          </div>
          <div class="card-text">
            <span class="meta">Year</span>
            <span class="value">2024 - 2028</span>
          </div>
        </div>
      </div>

      <p class="about-bio animate animate-delay-6">
        对机器学习和数据科学有浓厚兴趣，
        专注于将统计方法与软件工程结合，
        探索数据驱动的解决方案。
      </p>
    </div>
  </section>
</template>

<style scoped>
.about-grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 1.5rem;
  margin-bottom: 3rem;
}

.about-card {
  display: flex;
  align-items: center;
  gap: 1.25rem;
}

.card-icon {
  width: 48px;
  height: 48px;
  border-radius: 12px;
  background: var(--accent-subtle);
  color: var(--accent);
  display: flex;
  align-items: center;
  justify-content: center;
  flex-shrink: 0;
}

.card-text {
  display: flex;
  flex-direction: column;
  gap: 2px;
}

.card-text .meta {
  font-size: var(--text-sm);
  color: var(--text-muted);
  font-family: var(--font-mono);
  text-transform: uppercase;
  letter-spacing: .05em;
}

.card-text .value {
  font-size: var(--text-lg);
  font-weight: 600;
}

.about-bio {
  font-size: var(--text-lg);
  color: var(--text-secondary);
  line-height: 1.8;
  padding: 2rem;
  background: var(--bg-subtle);
  border-radius: 14px;
  border-left: 4px solid var(--accent);
}

@media (max-width: 768px) {
  .about-grid { grid-template-columns: 1fr; }
}
</style>