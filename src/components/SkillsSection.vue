<template>
  <section id="skills" class="section">
    <div class="content">
      <div class="section-header">
        <div class="animate"><span class="section-label">02 / 技能</span></div>
        <h2 class="section-title animate animate-delay-1">专业技能</h2>
        <p class="section-subtitle animate animate-delay-2">
          技术栈与工具 · 熟练度自评
        </p>
      </div>

      <div class="skills-grid">
        <!-- 进度条区 -->
        <div class="card skill-card animate animate-delay-2">
          <div class="skill-category">编程基础</div>
          <div class="skill-bars">
            <div class="skill-bar-row">
              <span class="skill-name">Python</span>
              <div class="skill-bar"><div class="skill-fill" style="width:90%"></div></div>
            </div>
            <div class="skill-bar-row">
              <span class="skill-name">SQL</span>
              <div class="skill-bar"><div class="skill-fill" style="width:85%"></div></div>
            </div>
            <div class="skill-bar-row">
              <span class="skill-name">R</span>
              <div class="skill-bar"><div class="skill-fill" style="width:75%"></div></div>
            </div>
            <div class="skill-bar-row">
              <span class="skill-name">Java</span>
              <div class="skill-bar"><div class="skill-fill" style="width:70%"></div></div>
            </div>
            <div class="skill-bar-row">
              <span class="skill-name">TypeScript</span>
              <div class="skill-bar"><div class="skill-fill" style="width:65%"></div></div>
            </div>
          </div>
        </div>

        <div class="card skill-card animate animate-delay-3">
          <div class="skill-category">机器学习</div>
          <div class="skill-bars">
            <div class="skill-bar-row">
              <span class="skill-name">Scikit-learn</span>
              <div class="skill-bar"><div class="skill-fill" style="width:85%"></div></div>
            </div>
            <div class="skill-bar-row">
              <span class="skill-name">PyTorch</span>
              <div class="skill-bar"><div class="skill-fill" style="width:80%"></div></div>
            </div>
            <div class="skill-bar-row">
              <span class="skill-name">Pandas</span>
              <div class="skill-bar"><div class="skill-fill" style="width:90%"></div></div>
            </div>
            <div class="skill-bar-row">
              <span class="skill-name">NumPy</span>
              <div class="skill-bar"><div class="skill-fill" style="width:88%"></div></div>
            </div>
            <div class="skill-bar-row">
              <span class="skill-name">TensorFlow</span>
              <div class="skill-bar"><div class="skill-fill" style="width:70%"></div></div>
            </div>
          </div>
        </div>

        <div class="card skill-card animate animate-delay-4">
          <div class="skill-category">数据分析 / 可视化</div>
          <div class="skill-bars">
            <div class="skill-bar-row">
              <span class="skill-name">Matplotlib</span>
              <div class="skill-bar"><div class="skill-fill" style="width:88%"></div></div>
            </div>
            <div class="skill-bar-row">
              <span class="skill-name">Seaborn</span>
              <div class="skill-bar"><div class="skill-fill" style="width:82%"></div></div>
            </div>
            <div class="skill-bar-row">
              <span class="skill-name">Hadoop</span>
              <div class="skill-bar"><div class="skill-fill" style="width:60%"></div></div>
            </div>
            <div class="skill-bar-row">
              <span class="skill-name">Spark</span>
              <div class="skill-bar"><div class="skill-fill" style="width:55%"></div></div>
            </div>
          </div>
        </div>

        <div class="card skill-card animate animate-delay-5">
          <div class="skill-category">开发工具</div>
          <div class="skill-bars">
            <div class="skill-bar-row">
              <span class="skill-name">Git</span>
              <div class="skill-bar"><div class="skill-fill" style="width:85%"></div></div>
            </div>
            <div class="skill-bar-row">
              <span class="skill-name">Linux</span>
              <div class="skill-bar"><div class="skill-fill" style="width:75%"></div></div>
            </div>
            <div class="skill-bar-row">
              <span class="skill-name">Docker</span>
              <div class="skill-bar"><div class="skill-fill" style="width:65%"></div></div>
            </div>
            <div class="skill-bar-row">
              <span class="skill-name">VS Code</span>
              <div class="skill-bar"><div class="skill-fill" style="width:92%"></div></div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.section {
  display: flex;
  flex-direction: column;
  justify-content: center;
  padding: 5rem 2rem;
}

.content {
  max-width: 1200px;
  width: 100%;
  margin: 0 auto;
}

.section-header { margin-bottom: 2.5rem; }

.section-label {
  font-family: var(--font-mono);
  font-size: var(--text-sm);
  font-weight: 500;
  color: var(--accent);
  text-transform: uppercase;
  letter-spacing: .08em;
  margin-bottom: .5rem;
  display: block;
}

.section-title {
  font-size: clamp(1.75rem, 4vw, 2.5rem);
  font-weight: 700;
  letter-spacing: -.03em;
  line-height: 1.15;
}

.section-subtitle {
  color: var(--text-secondary);
  margin-top: .5rem;
  font-size: var(--text-lg);
  font-weight: 400;
}

.skills-grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 1rem;
}

.skill-card {
  display: flex;
  flex-direction: column;
  gap: 1rem;
  padding: 1.25rem;
}

.skill-category {
  font-size: var(--text-lg);
  font-weight: 600;
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
  background: linear-gradient(90deg, var(--accent), #6366f1);
  border-radius: 999px;
  transition: width .6s var(--ease-out);
}

@media (max-width: 768px) {
  .section { padding: 4rem 1.25rem 3rem; justify-content: flex-start; }

  .skills-grid {
    grid-template-columns: 1fr;
    gap: .75rem;
  }

  .skill-card { padding: 1rem; }

  .skill-category { font-size: var(--text-base); }

  .skill-bar-row { gap: .5rem; }

  .skill-name { min-width: 70px; font-size: var(--text-xs); }

  .skill-bar { height: 5px; }
}
</style>
