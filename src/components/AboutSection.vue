<template>
  <section id="about" class="section">
    <div class="content">
      <div class="section-header">
        <div class="animate"><span class="section-label">01 / 关于</span></div>
        <h2 class="section-title animate animate-delay-1">关于我</h2>
        <p class="section-subtitle animate animate-delay-2">
          基本信息与自我介绍
        </p>
      </div>

      <div class="about-grid">
        <div class="card about-card animate animate-delay-2">
          <div class="card-icon">
            <svg width="22" height="22" fill="none" stroke="currentColor" stroke-width="2"><circle cx="12" cy="8" r="4"/><path d="M4 20c0-4 4-7 8-7s8 3 8 7"/></svg>
          </div>
          <div class="card-text">
            <span class="meta">姓名</span>
            <span class="value">Yue-xin G.</span>
          </div>
        </div>

        <div class="card about-card animate animate-delay-3">
          <div class="card-icon">
            <svg width="22" height="22" fill="none" stroke="currentColor" stroke-width="2"><path d="M12 2v20M2 12h20"/></svg>
          </div>
          <div class="card-text">
            <span class="meta">所在地</span>
            <span class="value">辽宁大连</span>
          </div>
        </div>

        <div class="card about-card animate animate-delay-4">
          <div class="card-icon">
            <svg width="22" height="22" fill="none" stroke="currentColor" stroke-width="2"><rect x="3" y="4" width="18" height="16" rx="2"/><path d="M16 2v4M8 2v4M3 10h18"/></svg>
          </div>
          <div class="card-text">
            <span class="meta">专业</span>
            <span class="value">数据科学与大数据技术</span>
          </div>
        </div>

        <div class="card about-card animate animate-delay-5">
          <div class="card-icon">
            <svg width="22" height="22" fill="none" stroke="currentColor" stroke-width="2"><circle cx="12" cy="12" r="10"/><path d="M12 6v6l4 2"/></svg>
          </div>
          <div class="card-text">
            <span class="meta">年级</span>
            <span class="value">2023 级 · 本科在读</span>
          </div>
        </div>
      </div>

      <p class="about-bio animate animate-delay-6">
        就读于大连海洋大学，对机器学习和数据科学有浓厚兴趣。
        专注于将统计方法与软件工程相结合，
        探索数据驱动的解决方案，热衷于用数据讲故事。
      </p>
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

.about-grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 1rem;
  margin-bottom: 2rem;
}

.about-card {
  display: flex;
  align-items: center;
  gap: 1rem;
  padding: 1.25rem;
}

.card-icon {
  width: 42px;
  height: 42px;
  border-radius: 10px;
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
  padding: 1.5rem;
  background: var(--bg-subtle);
  border-radius: 12px;
  border-left: 4px solid var(--accent);
}

@media (max-width: 768px) {
  .section {
    padding: 3rem 1.25rem;
  }

  .about-grid {
    grid-template-columns: 1fr;
    gap: .75rem;
    margin-bottom: 1.5rem;
  }

  .about-card {
    padding: 1rem;
  }

  .card-icon {
    width: 36px;
    height: 36px;
  }

  .card-text .value {
    font-size: var(--text-base);
  }

  .about-bio {
    padding: 1rem 1.25rem;
    font-size: var(--text-base);
  }
}
</style>