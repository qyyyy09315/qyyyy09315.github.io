<template>
  <section id="skills" class="section skills-section">
    <div class="content">
      <div class="section-header">
        <span class="section-label">02 / Skills</span>
        <h2 class="section-title">Technical Toolkit</h2>
        <p class="section-subtitle">Technologies and tools I work with</p>
      </div>

      <div class="skills-groups">
        <div class="skill-group card">
          <div class="group-header">
            <div class="group-icon languages-icon">
              <svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5"><polyline points="4 17 10 11 4 5"/><line x1="12" y1="19" x2="20" y2="19"/></svg>
            </div>
            <h3>Languages</h3>
          </div>
          <div class="group-tags">
            <span class="tag">Python</span>
            <span class="tag">R</span>
            <span class="tag">SQL</span>
          </div>
        </div>

        <div class="skill-group card">
          <div class="group-header">
            <div class="group-icon ml-icon">
              <svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5"><rect x="3" y="3" width="7" height="7" rx="1"/><rect x="14" y="3" width="7" height="7" rx="1"/><rect x="3" y="14" width="7" height="7" rx="1"/><rect x="14" y="14" width="7" height="7" rx="1"/></svg>
            </div>
            <h3>Machine Learning</h3>
          </div>
          <div class="group-tags">
            <span class="tag">Scikit-learn</span>
            <span class="tag">PyTorch</span>
            <span class="tag">TensorFlow</span>
            <span class="tag">Deep Learning</span>
          </div>
        </div>

        <div class="skill-group card">
          <div class="group-header">
            <div class="group-icon data-icon">
              <svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5"><ellipse cx="12" cy="5" rx="9" ry="3"/><path d="M3 5v14a9 3 0 0018 0V5"/><path d="M3 12a9 3 0 0018 0"/></svg>
            </div>
            <h3>Data & Analysis</h3>
          </div>
          <div class="group-tags">
            <span class="tag">Pandas</span>
            <span class="tag">NumPy</span>
            <span class="tag">Matplotlib</span>
            <span class="tag">Hadoop</span>
            <span class="tag">Spark</span>
          </div>
        </div>

        <div class="skill-group card">
          <div class="group-header">
            <div class="group-icon tools-icon">
              <svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5"><path d="M14.7 6.3a1 1 0 000 1.4l1.6 1.6a1 1 0 001.4 0l3.77-3.77a6 6 0 01-7.94 7.94l-6.91 6.91a2.12 2.12 0 01-3-3l6.91-6.91a6 6 0 017.94-7.94l-3.76 3.76z"/></svg>
            </div>
            <h3>Tools & Platforms</h3>
          </div>
          <div class="group-tags">
            <span class="tag">Git</span>
            <span class="tag">Linux</span>
            <span class="tag">Jupyter</span>
            <span class="tag">VS Code</span>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.skills-section {
  padding: 5rem 2rem;
  background: var(--bg-subtle);
}

.skills-groups {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 1rem;
}

.skill-group {
  display: flex;
  flex-direction: column;
  gap: 1.25rem;
}

.group-header {
  display: flex;
  align-items: center;
  gap: 0.75rem;
}

.group-icon {
  width: 36px;
  height: 36px;
  border-radius: 8px;
  display: flex;
  align-items: center;
  justify-content: center;
  color: var(--accent);
}

.languages-icon { background: #eff6ff; color: #2563eb; }
.ml-icon { background: #fdf4ff; color: #a21caf; }
.data-icon { background: #f0fdf4; color: #16a34a; }
.tools-icon { background: #fff7ed; color: #ea580c; }

.group-header h3 {
  font-size: 0.9375rem;
  font-weight: 600;
  letter-spacing: -0.01em;
}

.group-tags {
  display: flex;
  flex-wrap: wrap;
  gap: 0.5rem;
}

@media (max-width: 640px) {
  .skills-groups {
    grid-template-columns: 1fr;
  }
}
</style>
