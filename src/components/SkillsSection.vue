<template>
  <section id="skills" class="section">
    <div class="content">
      <div class="section-header">
        <div class="animate"><span class="section-label">02 / 技能</span></div>
        <h2 class="section-title animate animate-delay-1">专业技能</h2>
        <p class="section-subtitle animate animate-delay-2">
          技术栈与工具
        </p>
      </div>

      <div class="skills-grid">
        <div class="card skill-card animate animate-delay-2">
          <div class="skill-header">
            <span class="skill-icon">💻</span>
            <span class="skill-category">编程语言</span>
          </div>
          <div class="skill-tags">
            <span class="tag">Python</span>
            <span class="tag">R</span>
            <span class="tag">SQL</span>
            <span class="tag">Java</span>
          </div>
        </div>

        <div class="card skill-card animate animate-delay-3">
          <div class="skill-header">
            <span class="skill-icon">🤖</span>
            <span class="skill-category">机器学习</span>
          </div>
          <div class="skill-tags">
            <span class="tag">Scikit-learn</span>
            <span class="tag">PyTorch</span>
            <span class="tag">TensorFlow</span>
            <span class="tag">Pandas</span>
            <span class="tag">NumPy</span>
          </div>
        </div>

        <div class="card skill-card animate animate-delay-4">
          <div class="skill-header">
            <span class="skill-icon">📊</span>
            <span class="skill-category">数据分析</span>
          </div>
          <div class="skill-tags">
            <span class="tag">Matplotlib</span>
            <span class="tag">Seaborn</span>
            <span class="tag">Hadoop</span>
            <span class="tag">Spark</span>
          </div>
        </div>

        <div class="card skill-card animate animate-delay-5">
          <div class="skill-header">
            <span class="skill-icon">🛠️</span>
            <span class="skill-category">开发工具</span>
          </div>
          <div class="skill-tags">
            <span class="tag">Git</span>
            <span class="tag">Linux</span>
            <span class="tag">Docker</span>
            <span class="tag">VS Code</span>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.skills-grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 1.5rem;
}

.skill-card {
  display: flex;
  flex-direction: column;
  gap: 1.25rem;
  padding: var(--space-8);
}

.skill-header {
  display: flex;
  align-items: center;
  gap: .75rem;
}

.skill-icon {
  font-size: 1.5rem;
}

.skill-category {
  font-size: var(--text-lg);
  font-weight: 600;
}

.skill-tags {
  display: flex;
  flex-wrap: wrap;
  gap: .625rem;
}

@media (max-width: 768px) {
  .skills-grid { grid-template-columns: 1fr; }
}
</style>