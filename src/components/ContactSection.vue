<template>
  <section id="contact" class="section">
    <div class="content">
      <div class="section-header">
        <h2>Contact</h2>
        <p>联系方式</p>
      </div>
      <div class="contact-grid">
        <div class="contact-card">
          <div class="icon" v-html="contacts[0].icon"></div>
          <h3>{{ contacts[0].title }}</h3>
          <a :href="contacts[0].link">{{ contacts[0].value }}</a>
        </div>
        <div class="contact-card">
          <div class="icon" v-html="contacts[1].icon"></div>
          <h3>{{ contacts[1].title }}</h3>
          <a :href="contacts[1].link" target="_blank">{{ contacts[1].value }}</a>
        </div>
        <div class="contact-card">
          <div class="icon" v-html="contacts[2].icon"></div>
          <h3>{{ contacts[2].title }}</h3>
          <p>{{ contacts[2].value }}</p>
        </div>
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
    icon: '<svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><rect x="2" y="4" width="20" height="16" rx="2"/><polyline points="22,6 12,13 2,6"/></svg>'
  },
  {
    title: 'GitHub',
    value: 'github.com/qyyyy09315',
    link: 'https://github.com/qyyyy09315',
    icon: '<svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="currentColor"><path d="M12 0c-6.626 0-12 5.373-12 12 0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23.957-.266 1.983-.399 3.003-.404 1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v3.293c0 .319.192.694.801.576 4.765-1.589 8.199-6.086 8.199-11.386 0-6.627-5.373-12-12-12z"/></svg>'
  },
  {
    title: 'Location',
    value: 'Dalian, Liaoning, China',
    link: '#',
    icon: '<svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M21 10c0 7-9 13-9 13s-9-6-9-13a9 9 0 0118 0z"/><circle cx="12" cy="10" r="3"/></svg>'
  }
])
</script>

<style scoped>
.section {
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  padding: 6rem 0;
}

.content {
  max-width: 960px;
  width: 100%;
  margin: 0 auto;
  padding: 0 2rem;
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

.contact-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
  gap: 1.5rem;
}

.contact-card {
  padding: 1.5rem;
  background: #f9fafb;
  border-radius: 12px;
  border: 1px solid #e5e7eb;
  transition: border-color 0.2s, transform 0.2s;
}

.contact-card:hover {
  border-color: #2563eb;
  transform: translateY(-2px);
}

.icon {
  width: 40px;
  height: 40px;
  background: #eff6ff;
  border-radius: 8px;
  display: flex;
  align-items: center;
  justify-content: center;
  margin-bottom: 1rem;
  color: #2563eb;
}

.contact-card h3 {
  font-size: 0.875rem;
  font-weight: 600;
  margin-bottom: 0.25rem;
}

.contact-card a,
.contact-card p {
  font-size: 0.875rem;
  color: #6b7280;
  text-decoration: none;
}

.contact-card a:hover {
  color: #2563eb;
}
</style>