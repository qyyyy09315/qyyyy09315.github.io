<template>
  <section id="skills" class="section">
    <div class="content">
      <div class="section-header">
        <h2>Skills</h2>
        <p>专业技能</p>
      </div>
      <div class="skills-list">
        <span
          v-for="skill in skills"
          :key="skill"
          class="skill-tag"
        >
          {{ skill }}
        </span>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref } from 'vue'

const skills = ref([
  'Python', 'R', 'SQL', 'Machine Learning', 'Deep Learning',
  'Data Analysis', 'Pandas / NumPy', 'Scikit-learn', 'PyTorch',
  'TensorFlow', 'Matplotlib', 'Hadoop', 'Spark', 'Git', 'Linux',
  'Mathematical Modeling'
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

.skills-list {
  display: flex;
  flex-wrap: wrap;
  gap: 0.75rem;
}

.skill-tag {
  padding: 0.5rem 1rem;
  background: #eff6ff;
  color: #2563eb;
  border-radius: 6px;
  font-size: 0.875rem;
  font-weight: 500;
  transition: transform 0.2s;
  cursor: default;
}

.skill-tag:hover {
  transform: translateY(-2px);
}
</style>