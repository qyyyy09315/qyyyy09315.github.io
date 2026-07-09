<template>
  <section id="education" class="section education-section">
    <div class="content">
      <div class="section-header">
        <span class="section-label">03 / Education</span>
        <h2 class="section-title">Academic Background</h2>
      </div>

      <div class="edu-timeline">
        <div class="edu-card card">
          <div class="edu-card-inner">
            <div class="edu-year">
              <span class="year-badge">2024 — 2028</span>
            </div>
            <div class="edu-details">
              <h3 class="edu-school">Dalian Ocean University</h3>
              <p class="edu-degree">Bachelor of Science in Big Data Science</p>
              <div class="edu-meta">
                <span class="edu-tag">Undergraduate</span>
                <span class="edu-tag">Full-time</span>
              </div>
            </div>
          </div>
        </div>

        <div class="edu-card card">
          <div class="edu-card-inner">
            <div class="edu-year">
              <span class="year-badge">2021 — 2024</span>
            </div>
            <div class="edu-details">
              <h3 class="edu-school">High School Affiliated to Dalian University of Technology</h3>
              <p class="edu-degree">High School Diploma</p>
              <div class="edu-meta">
                <span class="edu-tag">Graduated</span>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.education-section {
  padding: 5rem 2rem;
}

.edu-timeline {
  display: flex;
  flex-direction: column;
  gap: 1rem;
  max-width: 720px;
}

.edu-card-inner {
  display: flex;
  gap: 2rem;
  align-items: flex-start;
}

.edu-year {
  flex-shrink: 0;
  min-width: 140px;
}

.year-badge {
  font-family: var(--font-mono);
  font-size: 0.8125rem;
  font-weight: 500;
  color: var(--text-muted);
  padding: 0.375rem 0.75rem;
  background: var(--bg-subtle);
  border: 1px solid var(--border-subtle);
  border-radius: 6px;
  display: inline-block;
}

.edu-details {
  flex: 1;
}

.edu-school {
  font-size: 1rem;
  font-weight: 600;
  letter-spacing: -0.01em;
  margin-bottom: 0.25rem;
}

.edu-degree {
  font-size: 0.875rem;
  color: var(--text-secondary);
  margin-bottom: 0.75rem;
}

.edu-meta {
  display: flex;
  gap: 0.5rem;
  flex-wrap: wrap;
}

.edu-tag {
  font-family: var(--font-mono);
  font-size: 0.6875rem;
  padding: 0.25rem 0.5rem;
  background: var(--accent-subtle);
  color: var(--accent);
  border-radius: 4px;
  font-weight: 500;
}

@media (max-width: 640px) {
  .edu-card-inner {
    flex-direction: column;
    gap: 1rem;
  }
}
</style>
