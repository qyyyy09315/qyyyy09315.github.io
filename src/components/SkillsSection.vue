<template>
  <section id="skills" class="section">
    <div class="decor-blob decor-blob--primary" style="width:280px;height:280px;top:-90px;right:-70px;"></div>
    <div class="decor-blob decor-blob--cyan" style="width:220px;height:220px;bottom:-70px;left:-70px;"></div>
    <div class="decor-shape decor-shape--cross" style="top:55%;right:8%;"></div>

    <div class="content" style="position:relative;z-index:1;">
      <div class="section-header animate fade-up">
        <h2 class="section-title">技能</h2>
      </div>

      <!-- 编程基础：带动画进度条 -->
      <div class="skills-grid">
        <div class="card skill-card animate fade-up" style="--delay: 0.1s">
          <div class="skill-category">
            <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M18 6L6 18M6 6l12 12"/></svg>
            编程基础
          </div>
          <div class="skill-bars">
            <div class="skill-bar-row"><span class="skill-name">Python</span><div class="skill-bar"><div class="skill-fill" style="--target:90%"></div></div><span class="skill-pct">90%</span></div>
            <div class="skill-bar-row"><span class="skill-name">SQL</span><div class="skill-bar"><div class="skill-fill" style="--target:85%"></div></div><span class="skill-pct">85%</span></div>
            <div class="skill-bar-row"><span class="skill-name">R</span><div class="skill-bar"><div class="skill-fill" style="--target:75%"></div></div><span class="skill-pct">75%</span></div>
            <div class="skill-bar-row"><span class="skill-name">Java</span><div class="skill-bar"><div class="skill-fill" style="--target:70%"></div></div><span class="skill-pct">70%</span></div>
            <div class="skill-bar-row"><span class="skill-name">TypeScript</span><div class="skill-bar"><div class="skill-fill" style="--target:65%"></div></div><span class="skill-pct">65%</span></div>
          </div>
        </div>

        <!-- 机器学习：标签云 + 熟练度圆环 -->
        <div class="card skill-card animate fade-up" style="--delay: 0.2s">
          <div class="skill-category">
            <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><rect x="3" y="3" width="18" height="18" rx="2"/><path d="M9 9h6v6H9z"/></svg>
            机器学习
          </div>
          <div class="skill-chips">
            <div class="skill-chip" style="--level: 85;">
              <span class="chip-name">Scikit-learn</span>
              <span class="chip-ring"><span class="chip-ring-fill"></span></span>
            </div>
            <div class="skill-chip" style="--level: 80;">
              <span class="chip-name">PyTorch</span>
              <span class="chip-ring"><span class="chip-ring-fill"></span></span>
            </div>
            <div class="skill-chip" style="--level: 90;">
              <span class="chip-name">Pandas</span>
              <span class="chip-ring"><span class="chip-ring-fill"></span></span>
            </div>
            <div class="skill-chip" style="--level: 88;">
              <span class="chip-name">NumPy</span>
              <span class="chip-ring"><span class="chip-ring-fill"></span></span>
            </div>
            <div class="skill-chip" style="--level: 70;">
              <span class="chip-name">TensorFlow</span>
              <span class="chip-ring"><span class="chip-ring-fill"></span></span>
            </div>
          </div>
        </div>

        <!-- 数据分析：水平进度条变体（带图标风格） -->
        <div class="card skill-card animate fade-up" style="--delay: 0.3s">
          <div class="skill-category">
            <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M3 3v18h18"/><path d="M18 17V9"/><path d="M13 17V5"/><path d="M8 17v-3"/></svg>
            数据分析
          </div>
          <div class="skill-meters">
            <div class="skill-meter">
              <div class="meter-label"><span>Matplotlib</span><span>88%</span></div>
              <div class="meter-track"><div class="meter-fill" style="--target:88%"></div></div>
            </div>
            <div class="skill-meter">
              <div class="meter-label"><span>Seaborn</span><span>82%</span></div>
              <div class="meter-track"><div class="meter-fill" style="--target:82%"></div></div>
            </div>
            <div class="skill-meter">
              <div class="meter-label"><span>Hadoop</span><span>60%</span></div>
              <div class="meter-track"><div class="meter-fill" style="--target:60%"></div></div>
            </div>
            <div class="skill-meter">
              <div class="meter-label"><span>Spark</span><span>55%</span></div>
              <div class="meter-track"><div class="meter-fill" style="--target:55%"></div></div>
            </div>
          </div>
        </div>

        <!-- 开发工具：极简标签列表 -->
        <div class="card skill-card animate fade-up" style="--delay: 0.4s">
          <div class="skill-category">
            <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M14.7 6.3a1 1 0 000 1.4l1.6 1.6a1 1 0 001.4 0l3.77-3.77a6 6 0 01-7.94 7.94l-6.91 6.91a2.12 2.12 0 01-3-3l6.91-6.91a6 6 0 017.94-7.94l-3.76 3.76z"/></svg>
            开发工具
          </div>
          <div class="skill-tools">
            <div class="tool-item">
              <span class="tool-bar"></span>
              <span class="tool-name">Git</span>
            </div>
            <div class="tool-item">
              <span class="tool-bar"></span>
              <span class="tool-name">Linux</span>
            </div>
            <div class="tool-item">
              <span class="tool-bar"></span>
              <span class="tool-name">Docker</span>
            </div>
            <div class="tool-item">
              <span class="tool-bar"></span>
              <span class="tool-name">Vibe Coding</span>
            </div>
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

/* === 2x2 Grid Layout === */
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

/* === 编程基础：经典进度条 === */
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
  width: 110px;
  flex-shrink: 0;
  white-space: nowrap;
  text-align: right;
}

.skill-bar {
  flex: 1;
  height: 6px;
  background: var(--border-subtle);
  border-radius: 999px;
  overflow: hidden;
}

.skill-fill {
  width: 0;
  height: 100%;
  background: linear-gradient(90deg, var(--accent), var(--accent-secondary));
  border-radius: 999px;
}

.skill-card.visible .skill-fill {
  animation: barGrow 1s cubic-bezier(0.22, 1, 0.36, 1) forwards;
  animation-delay: calc(var(--delay, 0s) + 0.3s);
}

@keyframes barGrow {
  from { width: 0; }
  to { width: var(--target); }
}

.skill-pct {
  font-family: var(--font-mono);
  font-size: var(--text-sm);
  color: var(--text-muted);
  width: 36px;
  flex-shrink: 0;
  text-align: right;
}

/* === 机器学习：标签云 + 圆环 === */
.skill-chips {
  display: flex;
  flex-direction: column;
  gap: .75rem;
}

.skill-chip {
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: .75rem;
}

.chip-name {
  font-size: var(--text-sm);
  color: var(--text-secondary);
  white-space: nowrap;
}

.chip-ring {
  width: 28px;
  height: 28px;
  border-radius: 50%;
  background: var(--border-subtle);
  display: flex;
  align-items: center;
  justify-content: center;
  flex-shrink: 0;
}

.chip-ring-fill {
  width: 0;
  height: 0;
  border-radius: 50%;
  background: var(--accent);
  transition: all 1s cubic-bezier(0.22, 1, 0.36, 1);
  transition-delay: calc(var(--delay, 0s) + 0.3s);
}

.skill-card.visible .chip-ring-fill {
  width: calc(var(--level) * 0.28px);
  height: calc(var(--level) * 0.28px);
  background: var(--accent);
  opacity: calc(0.3 + var(--level) * 0.007);
}

/* === 数据分析： meter 风格 === */
.skill-meters {
  display: flex;
  flex-direction: column;
  gap: .875rem;
}

.skill-meter {
  display: flex;
  flex-direction: column;
  gap: .375rem;
}

.meter-label {
  display: flex;
  justify-content: space-between;
  font-size: var(--text-sm);
  color: var(--text-secondary);
}

.meter-label span:first-child {
  font-family: var(--font-mono);
}

.meter-label span:last-child {
  color: var(--text-muted);
}

.meter-track {
  height: 8px;
  background: var(--border-subtle);
  border-radius: 4px;
  overflow: hidden;
}

.meter-fill {
  width: 0;
  height: 100%;
  background: linear-gradient(90deg, var(--accent), var(--accent-cyan));
  border-radius: 4px;
}

.skill-card.visible .meter-fill {
  animation: meterGrow 1s cubic-bezier(0.22, 1, 0.36, 1) forwards;
  animation-delay: calc(var(--delay, 0s) + 0.3s);
}

@keyframes meterGrow {
  from { width: 0; }
  to { width: var(--target); }
}

/* === 开发工具：极简标签 === */
.skill-tools {
  display: flex;
  flex-direction: column;
  gap: .75rem;
}

.tool-item {
  display: flex;
  align-items: center;
  gap: .75rem;
}

.tool-bar {
  width: 18px;
  height: 3px;
  background: var(--accent);
  border-radius: 2px;
  flex-shrink: 0;
}

.tool-name {
  font-size: var(--text-sm);
  color: var(--text-secondary);
}

/* === Mobile === */
@media (max-width: 768px) {
  .section { padding: 3rem 1.25rem; justify-content: flex-start; }

  .skills-grid {
    grid-template-columns: 1fr;
    gap: .75rem;
  }

  .skill-card { padding: 1rem; }

  .skill-name { width: 80px; font-size: var(--text-xs); white-space: nowrap; }

  .skill-bar { height: 5px; }
}
</style>
