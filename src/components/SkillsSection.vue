<template>
  <section id="skills" class="section">
    <div class="decor-blob decor-blob--yellow" style="width:260px;height:260px;top:-80px;right:-60px;"></div>
    <div class="decor-shape decor-shape--dot" style="top:60%;left:8%;"></div>

    <div class="content" style="position:relative;z-index:1;">
      <div
        class="section-header"
        v-motion
        :initial="{ opacity: 0, y: 30 }"
        :visible-once="{ opacity: 1, y: 0, transition: { duration: 600, ease: 'easeOut' } }"
      >
        <h2 class="section-title">技能</h2>
      </div>

      <div class="skills-grid" v-auto-animate="{ duration: 500, easing: 'ease-out' }">
        <div class="card skill-card" v-motion :initial="{ opacity: 0, y: 28 }" :visible-once="{ opacity: 1, y: 0, transition: { delay: 100, duration: 500, ease: 'easeOut' } }">
          <div class="skill-category">
            <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M18 6L6 18M6 6l12 12"/></svg>
            编程基础
          </div>
          <div class="skill-bars">
            <div class="skill-bar-row"><span class="skill-name">Python</span><div class="skill-bar"><div class="skill-fill" v-motion :initial="{ width: '0%' }" :visible-once="{ width: '90%', transition: { delay: 400, duration: 900, ease: [0.16, 1, 0.3, 1] } }"></div></div></div>
            <div class="skill-bar-row"><span class="skill-name">SQL</span><div class="skill-bar"><div class="skill-fill" v-motion :initial="{ width: '0%' }" :visible-once="{ width: '85%', transition: { delay: 500, duration: 800, ease: [0.16, 1, 0.3, 1] } }"></div></div></div>
            <div class="skill-bar-row"><span class="skill-name">R</span><div class="skill-bar"><div class="skill-fill" v-motion :initial="{ width: '0%' }" :visible-once="{ width: '75%', transition: { delay: 600, duration: 700, ease: [0.16, 1, 0.3, 1] } }"></div></div></div>
            <div class="skill-bar-row"><span class="skill-name">Java</span><div class="skill-bar"><div class="skill-fill" v-motion :initial="{ width: '0%' }" :visible-once="{ width: '70%', transition: { delay: 700, duration: 600, ease: [0.16, 1, 0.3, 1] } }"></div></div></div>
            <div class="skill-bar-row"><span class="skill-name">TypeScript</span><div class="skill-bar"><div class="skill-fill" v-motion :initial="{ width: '0%' }" :visible-once="{ width: '65%', transition: { delay: 800, duration: 500, ease: [0.16, 1, 0.3, 1] } }"></div></div></div>
          </div>
        </div>

        <div class="card skill-card" v-motion :initial="{ opacity: 0, y: 28 }" :visible-once="{ opacity: 1, y: 0, transition: { delay: 200, duration: 500, ease: 'easeOut' } }">
          <div class="skill-category">
            <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><rect x="3" y="3" width="18" height="18" rx="2"/><path d="M9 9h6v6H9z"/></svg>
            机器学习
          </div>
          <div class="skill-bars">
            <div class="skill-bar-row"><span class="skill-name">Scikit-learn</span><div class="skill-bar"><div class="skill-fill" v-motion :initial="{ width: '0%' }" :visible-once="{ width: '85%', transition: { delay: 500, duration: 800, ease: [0.16, 1, 0.3, 1] } }"></div></div></div>
            <div class="skill-bar-row"><span class="skill-name">PyTorch</span><div class="skill-bar"><div class="skill-fill" v-motion :initial="{ width: '0%' }" :visible-once="{ width: '80%', transition: { delay: 600, duration: 700, ease: [0.16, 1, 0.3, 1] } }"></div></div></div>
            <div class="skill-bar-row"><span class="skill-name">Pandas</span><div class="skill-bar"><div class="skill-fill" v-motion :initial="{ width: '0%' }" :visible-once="{ width: '90%', transition: { delay: 700, duration: 800, ease: [0.16, 1, 0.3, 1] } }"></div></div></div>
            <div class="skill-bar-row"><span class="skill-name">NumPy</span><div class="skill-bar"><div class="skill-fill" v-motion :initial="{ width: '0%' }" :visible-once="{ width: '88%', transition: { delay: 800, duration: 700, ease: [0.16, 1, 0.3, 1] } }"></div></div></div>
            <div class="skill-bar-row"><span class="skill-name">TensorFlow</span><div class="skill-bar"><div class="skill-fill" v-motion :initial="{ width: '0%' }" :visible-once="{ width: '70%', transition: { delay: 900, duration: 600, ease: [0.16, 1, 0.3, 1] } }"></div></div></div>
          </div>
        </div>

        <div class="card skill-card" v-motion :initial="{ opacity: 0, y: 28 }" :visible-once="{ opacity: 1, y: 0, transition: { delay: 300, duration: 500, ease: 'easeOut' } }">
          <div class="skill-category">
            <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M3 3v18h18"/><path d="M18 17V9"/><path d="M13 17V5"/><path d="M8 17v-3"/></svg>
            数据分析
          </div>
          <div class="skill-bars">
            <div class="skill-bar-row"><span class="skill-name">Matplotlib</span><div class="skill-bar"><div class="skill-fill" v-motion :initial="{ width: '0%' }" :visible-once="{ width: '88%', transition: { delay: 600, duration: 800, ease: [0.16, 1, 0.3, 1] } }"></div></div></div>
            <div class="skill-bar-row"><span class="skill-name">Seaborn</span><div class="skill-bar"><div class="skill-fill" v-motion :initial="{ width: '0%' }" :visible-once="{ width: '82%', transition: { delay: 700, duration: 700, ease: [0.16, 1, 0.3, 1] } }"></div></div></div>
            <div class="skill-bar-row"><span class="skill-name">Hadoop</span><div class="skill-bar"><div class="skill-fill" v-motion :initial="{ width: '0%' }" :visible-once="{ width: '60%', transition: { delay: 800, duration: 600, ease: [0.16, 1, 0.3, 1] } }"></div></div></div>
            <div class="skill-bar-row"><span class="skill-name">Spark</span><div class="skill-bar"><div class="skill-fill" v-motion :initial="{ width: '0%' }" :visible-once="{ width: '55%', transition: { delay: 900, duration: 500, ease: [0.16, 1, 0.3, 1] } }"></div></div></div>
          </div>
        </div>

        <div class="card skill-card" v-motion :initial="{ opacity: 0, y: 28 }" :visible-once="{ opacity: 1, y: 0, transition: { delay: 400, duration: 500, ease: 'easeOut' } }">
          <div class="skill-category">
            <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M14.7 6.3a1 1 0 000 1.4l1.6 1.6a1 1 0 001.4 0l3.77-3.77a6 6 0 01-7.94 7.94l-6.91 6.91a2.12 2.12 0 01-3-3l6.91-6.91a6 6 0 017.94-7.94l-3.76 3.76z"/></svg>
            开发工具
          </div>
          <div class="skill-bars">
            <div class="skill-bar-row"><span class="skill-name">Git</span><div class="skill-bar"><div class="skill-fill" v-motion :initial="{ width: '0%' }" :visible-once="{ width: '85%', transition: { delay: 700, duration: 800, ease: [0.16, 1, 0.3, 1] } }"></div></div></div>
            <div class="skill-bar-row"><span class="skill-name">Linux</span><div class="skill-bar"><div class="skill-fill" v-motion :initial="{ width: '0%' }" :visible-once="{ width: '75%', transition: { delay: 800, duration: 700, ease: [0.16, 1, 0.3, 1] } }"></div></div></div>
            <div class="skill-bar-row"><span class="skill-name">Docker</span><div class="skill-bar"><div class="skill-fill" v-motion :initial="{ width: '0%' }" :visible-once="{ width: '65%', transition: { delay: 900, duration: 600, ease: [0.16, 1, 0.3, 1] } }"></div></div></div>
            <div class="skill-bar-row"><span class="skill-name">VS Code</span><div class="skill-bar"><div class="skill-fill" v-motion :initial="{ width: '0%' }" :visible-once="{ width: '92%', transition: { delay: 1000, duration: 700, ease: [0.16, 1, 0.3, 1] } }"></div></div></div>
          </div>
        </div>
      </div>
    </div>

    <div class="section-divider"></div>
  </section>
</template>

<style scoped>
.section {
  display: flex;
  flex-direction: column;
  justify-content: center;
  padding: 4rem 2rem;
  position: relative;
  overflow: hidden;
}

.content {
  max-width: 1000px;
  width: 100%;
  margin: 0 auto;
}

.section-header { margin-bottom: 2rem; }

.section-title {
  font-size: clamp(1.5rem, 3.5vw, 2rem);
  font-weight: 600;
  letter-spacing: -.02em;
  line-height: 1.2;
}

.skills-grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 1rem;
  position: relative;
}

.skill-card {
  display: flex;
  flex-direction: column;
  gap: 1rem;
  padding: 1.25rem;
  background: var(--bg-subtle);
  border-radius: 10px;
}

.skill-category {
  display: flex;
  align-items: center;
  gap: .5rem;
  font-size: var(--text-base);
  font-weight: 600;
  color: var(--text);
}

.skill-category svg {
  color: var(--accent);
  flex-shrink: 0;
}

.skill-bars {
  display: flex;
  flex-direction: column;
  gap: .625rem;
}

.skill-bar-row {
  display: flex;
  align-items: center;
  gap: .75rem;
}

.skill-name {
  font-family: var(--font-mono);
  font-size: var(--text-sm);
  color: var(--text-secondary);
  min-width: 90px;
  flex-shrink: 0;
}

.skill-bar {
  flex: 1;
  height: 6px;
  background: var(--border-subtle);
  border-radius: 999px;
  overflow: hidden;
}

.skill-fill {
  height: 100%;
  background: linear-gradient(90deg, var(--accent), var(--accent-coral));
  border-radius: 999px;
  will-change: width;
}

@media (max-width: 768px) {
  .section { padding: 3rem 1.25rem; justify-content: flex-start; }

  .skills-grid {
    grid-template-columns: 1fr;
    gap: .75rem;
  }

  .skill-card { padding: 1rem; }

  .skill-name { min-width: 70px; font-size: var(--text-xs); }

  .skill-bar { height: 5px; }
}
</style>
