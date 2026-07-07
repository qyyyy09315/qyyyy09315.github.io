<template>
  <section id="about" class="section">
    <div class="section-header">
      <h2>About Me</h2>
      <p>关于我</p>
    </div>
    <div class="about-grid">
      <div class="about-item">
        <label>Name</label>
        <span>Yue-xin G.</span>
      </div>
      <div class="about-item">
        <label>Location</label>
        <span>Dalian, China</span>
      </div>
      <div class="about-item">
        <label>Major</label>
        <span>Big Data Science</span>
      </div>
      <div class="about-item">
        <label>Interests</label>
        <span>ML · Data Science · Math Modeling</span>
      </div>
    </div>
  </section>
</template>

<style scoped>
.section {
  padding: 4rem 0;
  border-top: 1px solid #e5e7eb;
}

.section-header {
  margin-bottom: 2.5rem;
}

.section-header h2 {
  font-size: 1.5rem;
  font-weight: 600;
  letter-spacing: -0.02em;
}

.section-header p {
  color: #6b7280;
  margin-top: 0.5rem;
  font-size: 0.9375rem;
}

.about-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  gap: 2rem;
}

.about-item label {
  display: block;
  font-size: 0.75rem;
  color: #6b7280;
  text-transform: uppercase;
  letter-spacing: 0.05em;
  margin-bottom: 0.25rem;
}

.about-item span {
  font-size: 0.9375rem;
  font-weight: 500;
}
</style>