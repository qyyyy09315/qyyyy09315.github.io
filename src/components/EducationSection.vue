<template>
  <section id="education" class="section">
    <div class="content">
      <div class="section-header">
        <div class="animate"><span class="section-label">03 / Education</span></div>
        <h2 class="section-title animate animate-delay-1">Academic Background</h2>
        <p class="section-subtitle animate animate-delay-2">
          教育背景
        </p>
      </div>

      <div class="edu-timeline">
        <div class="edu-card card animate animate-delay-2">
          <div class="edu-year">2024 — 2028</div>
          <h3 class="edu-school">Dalian Ocean University</h3>
          <p class="edu-major">Big Data Science · Bachelor of Science</p>
        </div>

        <div class="edu-card card animate animate-delay-3">
          <div class="edu-year">2021 — 2024</div>
          <h3 class="edu-school">High School Affiliated to Dalian University of Technology</h3>
          <p class="edu-major">High School Diploma</p>
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