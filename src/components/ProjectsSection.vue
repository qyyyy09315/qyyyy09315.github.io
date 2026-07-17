<template>
  <section id="projects" class="section">
    <div class="decor-blob decor-blob--cyan" style="width:320px;height:320px;top:-100px;left:-90px;"></div>
    <div class="decor-blob decor-blob--green" style="width:240px;height:240px;bottom:-80px;right:-80px;"></div>
    <div class="decor-shape decor-shape--ring" style="width:50px;height:50px;top:35%;left:12%;"></div>
    <div class="decor-shape decor-shape--dot" style="bottom:20%;right:10%;"></div>

    <div class="content" style="position:relative;z-index:1;">
      <div
        class="section-header"
        v-motion
        :initial="{ opacity: 0, y: 35 }"
        :visible-once="{ opacity: 1, y: 0, transition: { type: 'spring', stiffness: 90, damping: 18 } }"
      >
        <h2 class="section-title">个人 / 合作项目</h2>
      </div>

      <div class="projects-grid" v-auto-animate="{ duration: 500, easing: 'ease-out' }">
        <a
          v-for="(p, i) in repos"
          :key="p.name"
          :href="p.url"
          target="_blank"
          class="card project-card"
          v-motion
          :initial="{ opacity: 0, y: 35, scale: 0.95 }"
          :visible-once="{ opacity: 1, y: 0, scale: 1, transition: { delay: 150 + i * 80, duration: 500, ease: 'easeOut' } }"
        >
          <div class="project-head">
            <svg class="project-icon" width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M9 19c-5 1.5-5-2.5-7-3m14 6v-3.87a3.37 3.37 0 00-.94-2.61c3.14-.35 6.44-1.54 6.44-7A5.04 5.04 0 0020 4.77 5.06 5.06 0 0019.91 1S18.73.65 16 2.48a13.38 13.38 0 00-7 0C6.27.65 5.09 1 5.09 1A5.06 5.06 0 005 4.77a5.04 5.04 0 00-1.5 3.78c0 5.42 3.3 6.61 6.44 7A3.37 3.37 0 009 18.13V22"/></svg>
            <h3 class="project-name">{{ p.name }}</h3>
            <span v-if="p.lang" class="project-lang">{{ p.lang }}</span>
          </div>
          <p class="project-desc">{{ p.desc }}</p>
          <span class="project-link">前往 GitHub →</span>
        </a>
      </div>
    </div>

    <div class="section-divider"></div>
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

.projects-grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 1rem;
  position: relative;
}

.project-card {
  display: flex;
  flex-direction: column;
  gap: .625rem;
  padding: 1.25rem;
  background: var(--bg-subtle);
  border-radius: 10px;
  text-decoration: none;
  color: inherit;
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.project-card:hover {
  transform: translateY(-4px);
  box-shadow: var(--shadow-medium);
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
  font-size: var(--text-sm);
  font-weight: 600;
  flex: 1;
  word-break: break-all;
}

.project-lang {
  display: inline-block;
  font-family: var(--font-mono);
  font-size: var(--text-xs);
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
}

@media (max-width: 768px) {
  .section { padding: 3rem 1.25rem; justify-content: flex-start; }

  .projects-grid {
    grid-template-columns: 1fr;
    gap: .75rem;
  }

  .project-card { padding: 1rem; }
}
</style>
