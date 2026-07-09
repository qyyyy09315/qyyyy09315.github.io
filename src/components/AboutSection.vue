<template>
  <section id="about" class="section about-section">
    <div class="content">
      <div class="section-header">
        <span class="section-label">01 / About</span>
        <h2 class="section-title">Who I Am</h2>
      </div>

      <div class="about-grid">
        <div class="card about-card">
          <div class="card-icon">
            <svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5"><circle cx="12" cy="8" r="4"/><path d="M20 21a8 8 0 00-16 0"/></svg>
          </div>
          <div class="card-body">
            <span class="card-label">Name</span>
            <span class="card-value">Yue-xin G.</span>
          </div>
        </div>

        <div class="card about-card">
          <div class="card-icon">
            <svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5"><path d="M21 10c0 7-9 13-9 13s-9-6-9-13a9 9 0 0118 0z"/><circle cx="12" cy="10" r="3"/></svg>
          </div>
          <div class="card-body">
            <span class="card-label">Location</span>
            <span class="card-value">Dalian, China</span>
          </div>
        </div>

        <div class="card about-card">
          <div class="card-icon">
            <svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5"><path d="M22 10v6M2 10l10-5 10 5-10 5z"/><path d="M6 12v5c0 2 3 3 6 3s6-1 6-3v-5"/></svg>
          </div>
          <div class="card-body">
            <span class="card-label">Major</span>
            <span class="card-value">Big Data Science</span>
          </div>
        </div>

        <div class="card about-card">
          <div class="card-icon">
            <svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5"><path d="M12 2L15.09 8.26L22 9.27L17 14.14L18.18 21.02L12 17.77L5.82 21.02L7 14.14L2 9.27L8.91 8.26L12 2z"/></svg>
          </div>
          <div class="card-body">
            <span class="card-label">Interests</span>
            <span class="card-value">ML · Data Science · Math Modeling</span>
          </div>
        </div>
      </div>

      <!-- Bio paragraph -->
      <div class="about-bio">
        <p>
          I'm an undergraduate student passionate about transforming raw data into meaningful insights.
          My curiosity lives at the intersection of statistics, algorithms, and elegant code —
          building things that make sense of complex information.
        </p>
      </div>
    </div>
  </section>
</template>

<style scoped>
.about-section {
  padding: 5rem 2rem;
}

.about-grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 1rem;
  margin-bottom: 3rem;
}

.about-card {
  display: flex;
  align-items: center;
  gap: 1rem;
  padding: 1.25rem;
}

.card-icon {
  width: 40px;
  height: 40px;
  border-radius: 10px;
  background: var(--bg-subtle);
  border: 1px solid var(--border-subtle);
  display: flex;
  align-items: center;
  justify-content: center;
  color: var(--accent);
  flex-shrink: 0;
}

.card-body {
  display: flex;
  flex-direction: column;
  gap: 2px;
}

.card-label {
  font-size: 0.6875rem;
  color: var(--text-muted);
  text-transform: uppercase;
  letter-spacing: 0.06em;
  font-family: var(--font-mono);
}

.card-value {
  font-size: 0.9375rem;
  font-weight: 500;
  color: var(--text);
}

.about-bio {
  max-width: var(--content-narrow);
}

.about-bio p {
  font-size: 1.0625rem;
  line-height: 1.8;
  color: var(--text-secondary);
  letter-spacing: -0.01em;
}

@media (max-width: 640px) {
  .about-grid {
    grid-template-columns: 1fr;
  }
}
</style>
