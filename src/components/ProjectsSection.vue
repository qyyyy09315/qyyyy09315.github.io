<template>
  <section id="projects" class="section">
    <div class="content">
      <div class="section-header">
        <div class="animate"><span class="section-label">03 / 项目</span></div>
        <h2 class="section-title animate animate-delay-1">项目经历</h2>
        <p class="section-subtitle animate animate-delay-2">
          开源项目与数据实践
        </p>
      </div>

      <div class="projects-grid">
        <a
          v-for="(p, i) in repos"
          :key="p.name"
          :href="p.url"
          target="_blank"
          class="card project-card"
          :class="`animate animate-delay-${Math.min(i + 2, 6)}`"
        >
          <div class="project-head">
            <svg class="project-icon" width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M9 19c-5 1.5-5-2.5-7-3m14 6v-3.87a3.37 3.37 0 00-.94-2.61c3.14-.35 6.44-1.54 6.44-7A5.04 5.04 0 0020 4.77 5.06 5.06 0 0019.91 1S18.73.65 16 2.48a13.38 13.38 0 00-7 0C6.27.65 5.09 1 5.09 1A5.06 5.06 0 005 4.77a5.04 5.04 0 00-1.5 3.78c0 5.42 3.3 6.61 6.44 7A3.37 3.37 0 009 18.13V22"/></svg>
            <h3 class="project-name">{{ p.name }}</h3>
            <span v-if="p.lang" class="project-lang">{{ p.lang }}</span>
          </div>
          <p class="project-desc">{{ p.desc }}</p>
          <span class="project-link">
            前往 GitHub
            <svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M7 17L17 7M17 7H7M17 7v10"/></svg>
          </span>
        </a>
      </div>
    </div>
  </section>
</template>

<script setup>
const repos = [
  {
    name: 'floral-notepaper',
    desc: '花笺，轻量优雅的跨平台桌面便签工具，支持 Markdown 编辑与预览',
    lang: null,
    url: 'https://github.com/qyyyy09315/floral-notepaper'
  },
  {
    name: 'Maze-Micromouse-Simulation',
    desc: 'TypeScript 实现的迷宫寻路仿真项目，模拟智能鼠走迷宫的算法验证',
    lang: 'TypeScript',
    url: 'https://github.com/qyyyy09315/Maze-Micromouse-Simulation'
  },
  {
    name: 'threejs-galaxy-visualization',
    desc: '基于 Three.js 的星系图前端可视化 skill，通用星图渲染与交互方案',
    lang: null,
    url: 'https://github.com/qyyyy09315/threejs-galaxy-visualization'
  },
  {
    name: 'Github-Remark-Reborn',
    desc: '为 GitHub 用户增加备注名的浏览器插件（JS，浏览器扩展）',
    lang: 'JavaScript',
    url: 'https://github.com/qyyyy09315/Github-Remark-Reborn'
  },
  {
    name: 'DophinCup2025ofSanX',
    desc: '三夏团队对 2025 海豚杯数据分析方法（Python，赛事数据分析）',
    lang: 'Python',
    url: 'https://github.com/qyyyy09315/DophinCup2025ofSanX'
  }
]
</script>

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

.projects-grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 1rem;
}

.project-card {
  display: flex;
  flex-direction: column;
  gap: .75rem;
  padding: 1.25rem;
  text-decoration: none;
  color: inherit;
  transition: transform var(--duration-fast) var(--ease-out),
              box-shadow var(--duration-fast) var(--ease-out);
}

.project-card:hover {
  transform: translateY(-3px);
  box-shadow: 0 8px 24px rgba(0, 0, 0, .06);
}

.project-head {
  display: flex;
  align-items: center;
  gap: .5rem;
}

.project-icon {
  color: var(--text-muted);
  flex-shrink: 0;
}

.project-name {
  font-family: var(--font-mono);
  font-size: var(--text-base);
  font-weight: 600;
  flex: 1;
  word-break: break-all;
}

.project-lang {
  display: inline-block;
  font-family: var(--font-mono);
  font-size: var(--text-sm);
  color: var(--accent);
  background: var(--accent-subtle);
  padding: .125rem .5rem;
  border-radius: 4px;
  white-space: nowrap;
}

.project-desc {
  font-size: var(--text-sm);
  color: var(--text-secondary);
  line-height: 1.6;
  flex: 1;
}

.project-link {
  font-family: var(--font-mono);
  font-size: var(--text-sm);
  color: var(--accent);
  display: inline-flex;
  align-items: center;
  gap: .25rem;
}

@media (max-width: 768px) {
  .section { padding: 4rem 1.25rem 3rem; justify-content: flex-start; }

  .projects-grid {
    grid-template-columns: 1fr;
    gap: .75rem;
  }

  .project-card { padding: 1rem; }
}
</style>
