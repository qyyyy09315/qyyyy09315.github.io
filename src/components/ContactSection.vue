<template>
  <section id="contact" class="section">
    <div class="content">
      <div class="section-header">
        <div class="animate"><span class="section-label">04 / Contact</span></div>
        <h2 class="section-title animate animate-delay-1">Get in Touch</h2>
        <p class="section-subtitle animate animate-delay-2">
          联系方式
        </p>
      </div>

      <div class="contact-grid">
        <div class="card contact-card animate animate-delay-2">
          <div class="contact-icon">
            <svg width="22" height="22" fill="none" stroke="currentColor" stroke-width="2"><rect x="2" y="4" width="20" height="16" rx="2"/><polyline points="22,6 12,13 2,6"/></svg>
          </div>
          <span class="contact-label">Email</span>
          <a href="mailto:contact@example.com" class="contact-value">contact@example.com</a>
        </div>

        <div class="card contact-card animate animate-delay-3">
          <div class="contact-icon">
            <svg width="22" height="22" fill="none" stroke="currentColor" stroke-width="2"><path d="M16 8a6 6 0 016 6v7h-4v-7a2 2 0 10-4 0v7h-4v-7a6 6 0 016-6zM2 9h4v12H2zM4 2a2 2 0 110 4 2 2 0 010-4z"/></svg>
          </div>
          <span class="contact-label">LinkedIn</span>
          <a href="#" class="contact-value">linkedin.com/in/yue-xin</a>
        </div>

        <div class="card contact-card animate animate-delay-4">
          <div class="contact-icon">
            <svg width="22" height="22" fill="none" stroke="currentColor" stroke-width="2"><path d="M9 19c-5 1.5-5-2.5-7-3m14 6v-3.87a3.37 3.37 0 00-.94-2.61c3.14-.35 6.44-1.54 6.44-7A5.04 5.04 0 0020 4.77 5.06 5.06 0 0019.91 1S18.73.65 16 2.48a13.38 13.38 0 00-7 0C6.27.65 5.09 1 5.09 1A5.06 5.06 0 005 4.77a5.04 5.04 0 00-1.5 3.78c0 5.42 3.3 6.61 6.44 7A3.37 3.37 0 009 18.13V22"/></svg>
          </div>
          <span class="contact-label">GitHub</span>
          <a href="https://github.com/qyyyy09315" class="contact-value">github.com/qyyyy09315</a>
        </div>

        <div class="card contact-card animate animate-delay-5">
          <div class="contact-icon">
            <svg width="22" height="22" fill="none" stroke="currentColor" stroke-width="2"><path d="M21 10c0 7-9 13-9 13s-9-6-9-13a9 9 0 0118 0z"/><circle cx="12" cy="10" r="3"/></svg>
          </div>
          <span class="contact-label">Location</span>
          <span class="contact-value">Dalian, China</span>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.contact-grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 1.5rem;
}

.contact-card {
  display: flex;
  flex-direction: column;
  gap: .5rem;
}

.contact-icon {
  width: 44px;
  height: 44px;
  border-radius: 10px;
  background: var(--accent-subtle);
  color: var(--accent);
  display: flex;
  align-items: center;
  justify-content: center;
  margin-bottom: .5rem;
}

.contact-label {
  font-size: var(--text-sm);
  color: var(--text-muted);
  font-family: var(--font-mono);
  text-transform: uppercase;
  letter-spacing: .05em;
}

.contact-value {
  font-size: var(--text-lg);
  font-weight: 600;
  color: var(--text);
  text-decoration: none;
}

.contact-value:hover {
  color: var(--accent);
}

@media (max-width: 768px) {
  .contact-grid { grid-template-columns: 1fr; }
}
</style>