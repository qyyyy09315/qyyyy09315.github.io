<template>
  <section class="section" id="about">
    <!-- Decorative elements - brighter and larger -->
    <div class="decor-blob decor-blob--rose" style="width:350px;height:350px;bottom:-120px;right:-90px;"></div>
    <div class="decor-shape decor-shape--ring" style="width:90px;height:90px;top:18%;left:4%;"></div>
    <div class="decor-shape decor-shape--dot" style="top:65%;left:15%;"></div>

    <div class="content" style="position:relative;z-index:1;">
      <div class="section-header animate fade-up">
        <h2 class="section-title">关于</h2>
      </div>

      <div class="about-opening animate fade-up" style="--delay: 0.15s">
        <p class="about-lead">
          数据科学与大数据技术专业本科在读，研究方向为
          <span class="highlight-punct"><span class="highlight">机器学习理论</span><span class="punct">、</span></span>
          <span class="highlight-punct"><span class="highlight">深度学习应用</span><span class="punct">、</span></span>
          <span class="highlight-punct"><span class="highlight">数学建模</span><span class="punct">。</span></span>
        </p>
      </div>

      <!-- Two-column layout: Current Focus + Beyond Work -->
      <div class="about-grid">
        <!-- Current Focus -->
        <div class="about-card focus-card animate fade-left" style="--delay: 0.3s">
          <div class="card-header">
            <svg class="card-icon" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><circle cx="12" cy="12" r="10"/><path d="M12 6v6l4 2"/></svg>
            <h3 class="card-title">当前焦点</h3>
          </div>
          <ul class="focus-list">
            <li class="focus-item">
              <span class="focus-dot"></span>
              <span>PLC 的仿真和应用研究（与自动化专业合作）</span>
            </li>
            <li class="focus-item">
              <span class="focus-dot"></span>
              <span>生物遗传代谢组学大数据研究</span>
            </li>
            <li class="focus-item">
              <span class="focus-dot"></span>
              <span>工业故障检测研究</span>
            </li>
            <li class="focus-item">
              <span class="focus-dot"></span>
              <span>自然语言的表示元学习应用研究</span>
            </li>
          </ul>
        </div>

        <!-- Beyond Work -->
        <div class="about-card beyond-card animate fade-right" style="--delay: 0.45s">
          <div class="card-header">
            <svg class="card-icon" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M12 2L2 7l10 5 10-5-10-5zM2 17l10 5 10-5M2 12l10 5 10-5"/></svg>
            <h3 class="card-title">工作之外</h3>
          </div>
          <div class="beyond-items">
            <div class="beyond-item">
              <span class="beyond-icon">⛏️</span>
              <span class="beyond-text">爱玩 <strong>Minecraft</strong></span>
            </div>
            <div class="beyond-item">
              <span class="beyond-icon">🏸</span>
              <span class="beyond-text">爱打 <strong>羽毛球</strong></span>
            </div>
          </div>
        </div>
      </div>

      <!-- CTA -->
      <div class="about-cta animate fade-up" style="--delay: 0.6s">
        <button class="btn btn-primary" @click="navTo(5)">
          <span>联系我</span>
          <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M7 17L17 7M17 7H7M17 7v10"/></svg>
        </button>
      </div>
    </div>

    <div class="section-divider"></div>
  </section>
</template>

<script setup>
import { inject } from 'vue'
const navTo = inject('navigateTo', () => {})
</script>

<style scoped>
.section {
  display: flex;
  flex-direction: column;
  justify-content: center;
  padding: 4rem 2rem;
  position: relative;
}

.content {
  max-width: 900px;
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

.about-opening { margin-bottom: 2.5rem; }

.about-lead {
  font-size: var(--text-lg);
  color: var(--text-secondary);
  line-height: 1.8;
}

.highlight {
  color: var(--accent);
  font-weight: 600;
  position: relative;
  display: inline-block;
}

.highlight::after {
  content: '';
  position: absolute;
  bottom: 2px;
  left: 0;
  right: 0;
  height: 6px;
  background: var(--accent-subtle);
  border-radius: 2px;
  z-index: -1;
}

/* 中文标点悬挂：避免行首出现标点符号 */
.punct {
  display: inline-block;
  text-indent: 0;
  margin-left: -0.05em;
  font-family: 'PingFang SC', 'Microsoft YaHei', sans-serif;
}

.about-grid {
  display: grid;
  grid-template-columns: 1.4fr 1fr;
  gap: 1.25rem;
  margin-bottom: 2.5rem;
}

.about-card {
  padding: 1.5rem;
  background: var(--bg-subtle);
  border-radius: 12px;
  border: 1px solid var(--border-subtle);
}

.card-header {
  display: flex;
  align-items: center;
  gap: .625rem;
  margin-bottom: 1.25rem;
}

.card-icon {
  color: var(--accent);
  flex-shrink: 0;
}

.card-title {
  font-size: var(--text-base);
  font-weight: 600;
  color: var(--text);
}

.focus-list {
  display: flex;
  flex-direction: column;
  gap: .75rem;
  list-style: none;
  padding: 0;
  margin: 0;
}

.focus-item {
  display: flex;
  align-items: flex-start;
  gap: .625rem;
  font-size: var(--text-sm);
  color: var(--text-secondary);
  line-height: 1.6;
}

.focus-dot {
  width: 6px;
  height: 6px;
  border-radius: 50%;
  background: var(--accent);
  flex-shrink: 0;
  margin-top: .5rem;
}

.beyond-items {
  display: flex;
  flex-direction: column;
  gap: 1rem;
}

.beyond-item {
  display: flex;
  align-items: center;
  gap: .75rem;
  padding: .75rem 1rem;
  background: var(--bg-elevated);
  border-radius: 8px;
  border: 1px solid var(--border-subtle);
}

.beyond-icon {
  font-size: 1.5rem;
  line-height: 1;
}

.beyond-text {
  font-size: var(--text-sm);
  color: var(--text-secondary);
}

.beyond-text strong {
  color: var(--text);
  font-weight: 600;
}

.about-cta {
  display: flex;
  justify-content: flex-start;
}

@media (max-width: 768px) {
  .section { padding: 3rem 1.25rem; justify-content: flex-start; }
  .section-title { font-size: var(--text-xl); }
  .about-lead { font-size: var(--text-base); }
  .about-grid { grid-template-columns: 1fr; gap: 1rem; }
  .about-card { padding: 1.25rem; }
  .decor-blob { opacity: 0.3; }
}
</style>
