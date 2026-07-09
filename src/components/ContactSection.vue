<template>
  <section id="contact" class="section contact-section">
    <div class="content">
      <div class="section-header">
        <span class="section-label">04 / Contact</span>
        <h2 class="section-title">Let's Connect</h2>
        <p class="section-subtitle">Feel free to reach out for collaborations or just a friendly hello</p>
      </div>

      <div class="contact-grid">
        <a
          v-for="contact in contacts"
          :key="contact.title"
          :href="contact.link"
          :target="contact.external ? '_blank' : undefined"
          class="contact-card card"
        >
          <div class="contact-icon" v-html="contact.icon"></div>
          <div class="contact-info">
            <span class="contact-label">{{ contact.title }}</span>
            <span class="contact-value">{{ contact.value }}</span>
          </div>
          <div class="contact-arrow">
            <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5"><path d="M7 17L17 7M17 7H7M17 7v10"/></svg>
          </div>
        </a>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref } from 'vue'

const contacts = ref([
  {
    title: 'Email',
    value: 'contact@example.com',
    link: 'mailto:contact@example.com',
    external: false,
    icon: '<svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5"><rect x="2" y="4" width="20" height="16" rx="2"/><polyline points="22,6 12,13 2,6"/></svg>'
  },
  {
    title: 'GitHub',
    value: 'github.com/qyyyy09315',
    link: 'https://github.com/qyyyy09315',
    external: true,
    icon: '<svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="currentColor"><path d="M12 0c-6.626 0-12 5.373-12 12 0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23.957-.266 1.983-.399 3.003-.404 1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v3.293c0 .319.192.694.801.576 4.765-1.589 8.199-6.086 8.199-11.386 0-6.627-5.373-12-12-12z"/></svg>'
  },
  {
    title: 'Location',
    value: 'Dalian, Liaoning, China',
    link: '#',
    external: false,
    icon: '<svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5"><path d="M21 10c0 7-9 13-9 13s-9-6-9-13a9 9 0 0118 0z"/><circle cx="12" cy="10" r="3"/></svg>'
  }
])
</script>

<style scoped>
.contact-section {
  padding: 5rem 2rem;
  background: var(--bg-subtle);
}

.contact-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 1rem;
  max-width: 900px;
}

.contact-card {
  display: flex;
  flex-direction: column;
  gap: 1rem;
  text-decoration: none;
  color: inherit;
}

.contact-icon {
  width: 40px;
  height: 40px;
  border-radius: 10px;
  background: var(--bg);
  border: 1px solid var(--border-subtle);
  display: flex;
  align-items: center;
  justify-content: center;
  color: var(--accent);
}

.contact-info {
  display: flex;
  flex-direction: column;
  gap: 2px;
}

.contact-label {
  font-size: 0.6875rem;
  color: var(--text-muted);
  text-transform: uppercase;
  letter-spacing: 0.06em;
  font-family: var(--font-mono);
}

.contact-value {
  font-size: 0.875rem;
  font-weight: 500;
  color: var(--text);
  word-break: break-all;
}

.contact-arrow {
  margin-left: auto;
  color: var(--text-muted);
  transition: all var(--duration-normal) var(--ease-out);
}

.contact-card:hover .contact-arrow {
  color: var(--accent);
  transform: translate(2px, -2px);
}

@media (max-width: 768px) {
  .contact-grid {
    grid-template-columns: 1fr;
  }
}
</style>
