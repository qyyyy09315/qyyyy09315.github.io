<template>
  <section class="section" id="about">
    <div class="content">
      <div class="section-header">
        <h2 class="section-title">关于</h2>
      </div>

      <p class="about-bio">
        就读于大连海洋大学，对机器学习和数据科学有浓厚兴趣。专注于将统计方法与软件工程相结合，探索数据驱动的解决方案，热衷于用数据讲故事。
      </p>
    </div>
  </section>
</template>

<style scoped>
.section {
  display: flex;
  flex-direction: column;
  justify-content: center;
  padding: 4rem 2rem;
}

.content {
  max-width: 720px;
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
}
</style>
