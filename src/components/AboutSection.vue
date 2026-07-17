<template>
  <section class="section" id="about">
    <div class="decor-blob decor-blob--coral" style="width:320px;height:320px;bottom:-100px;right:-80px;"></div>
    <div class="decor-shape decor-shape--ring" style="width:80px;height:80px;top:20%;left:5%;"></div>

    <div class="content" style="position:relative;z-index:1;">
      <div
        class="section-header"
        v-motion
        :initial="{ opacity: 0, y: 30 }"
        :visible-once="{ opacity: 1, y: 0, transition: { duration: 600, ease: 'easeOut' } }"
      >
        <h2 class="section-title">关于</h2>
      </div>

      <p
        class="about-bio"
        v-motion
        :initial="{ opacity: 0, y: 24 }"
        :visible-once="{ opacity: 1, y: 0, transition: { delay: 150, duration: 500, ease: 'easeOut' } }"
      >
        就读于大连海洋大学，对机器学习和数据科学有浓厚兴趣。专注于将统计方法与软件工程相结合，探索数据驱动的解决方案，热衷于用数据讲故事。
      </p>
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
  max-width: 900px;
  width: 100%;
  margin: 0 auto;
}

.section-header {
  margin-bottom: 2rem;
}

.section-title {
  font-size: clamp(1.5rem, 3.5vw, 2rem);
  font-weight: 600;
  letter-spacing: -.02em;
  line-height: 1.2;
}

.about-bio {
  font-size: var(--text-lg);
  color: var(--text-secondary);
  line-height: 1.8;
}

@media (max-width: 768px) {
  .section { padding: 3rem 1.25rem; justify-content: flex-start; }
  .section-title { font-size: var(--text-xl); }
  .about-bio { font-size: var(--text-base); }
  .decor-blob { opacity: 0.2; }
}
</style>
