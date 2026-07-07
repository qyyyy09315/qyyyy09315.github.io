<template>
  <section id="education" class="section">
    <div class="section-header">
      <h2>Education</h2>
      <p>教育背景</p>
    </div>
    <div class="edu-list">
      <div
        v-for="item in education"
        :key="item.school"
        class="edu-item"
      >
        <div>
          <div class="edu-school">{{ item.school }}</div>
          <div class="edu-major">{{ item.major }}</div>
        </div>
        <span class="edu-year">{{ item.year }}</span>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref } from 'vue'

const education = ref([
  {
    school: 'Dalian Ocean University',
    major: 'Bachelor of Science in Big Data Science',
    year: '2024 - 2028'
  },
  {
    school: 'High School Affiliated to Dalian University of Technology',
    major: 'High School Diploma',
    year: '2021 - 2024'
  }
])
</script>

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

.edu-item {
  display: flex;
  justify-content: space-between;
  align-items: baseline;
  padding: 1.25rem 0;
  border-bottom: 1px solid #e5e7eb;
}

.edu-item:last-child {
  border-bottom: none;
}

.edu-school {
  font-weight: 500;
  font-size: 0.9375rem;
}

.edu-major {
  font-size: 0.875rem;
  color: #6b7280;
  margin-top: 0.25rem;
}

.edu-year {
  font-size: 0.875rem;
  color: #6b7280;
  white-space: nowrap;
  margin-left: 2rem;
}

@media (max-width: 640px) {
  .edu-item {
    flex-direction: column;
  }

  .edu-year {
    margin-left: 0;
    margin-top: 0.5rem;
  }
}
</style>