<template>
  <section class="section" id="contact">
    <div class="decor-blob decor-blob--indigo" style="width:340px;height:340px;top:-100px;right:-80px;"></div>
    <div class="decor-blob decor-blob--rose" style="width:280px;height:280px;bottom:-90px;left:-80px;"></div>
    <div class="decor-shape decor-shape--ring" style="width:70px;height:70px;top:30%;left:8%;border-color: var(--accent-secondary);"></div>
    <div class="decor-shape decor-shape--dot" style="top:65%;right:14%;"></div>
    <div class="decor-shape decor-shape--cross" style="bottom:20%;left:6%;"></div>

    <div class="content" style="position:relative;z-index:1;">
      <div
        v-motion
        class="section-header"
        :initial="{ opacity: 0, y: 30 }"
        :visible-once="{ opacity: 1, y: 0, transition: { duration: 500, ease: 'easeOut' } }"
      >
        <h2 class="section-title">联系</h2>
      </div>

      <div class="emails-list">
        <div class="email-card">
          <div class="email-header">
            <svg class="email-icon" width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M4 4h16c1.1 0 2 .9 2 2v12c0 1.1-.9 2-2 2H4c-1.1 0-2-.9-2-2V6c0-1.1.9-2 2-2z"/><polyline points="22,6 12,13 2,6"/></svg>
            <div class="email-info">
              <span class="email-type">工作 / 业务</span>
              <a href="mailto:gengyuexin@qq.com" class="email-addr">gengyuexin@qq.com</a>
              <span class="email-note">业务合作 / 工作机会</span>
            </div>
          </div>
        </div>

        <div class="email-card">
          <div class="email-header">
            <svg class="email-icon" width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M4 4h16c1.1 0 2 .9 2 2v12c0 1.1-.9 2-2 2H4c-1.1 0-2-.9-2-2V6c0-1.1.9-2 2-2z"/><polyline points="22,6 12,13 2,6"/></svg>
            <div class="email-info">
              <span class="email-type">日常</span>
              <a href="mailto:ykshboy@163.com" class="email-addr">ykshboy@163.com</a>
              <span class="email-note">日常使用，不经常查看</span>
            </div>
          </div>
        </div>

        <div class="email-card">
          <div class="email-header">
            <svg class="email-icon" width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M4 4h16c1.1 0 2 .9 2 2v12c0 1.1-.9 2-2 2H4c-1.1 0-2-.9-2-2V6c0-1.1.9-2 2-2z"/><polyline points="22,6 12,13 2,6"/></svg>
            <div class="email-info">
              <span class="email-type">Agent</span>
              <a href="mailto:qyyyy09315@agent.qq.com" class="email-addr">qyyyy09315@agent.qq.com</a>
              <span class="email-note">每天查看，日常使用</span>
            </div>
          </div>
        </div>
      </div>

      <div class="contact-row">
        <div class="contact-item">
          <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M9 19c-5 1.5-5-2.5-7-3m14 6v-3.87a3.37 3.37 0 00-.94-2.61c3.14-.35 6.44-1.54 6.44-7A5.04 5.04 0 0020 4.77 5.06 5.06 0 0019.91 1S18.73.65 16 2.48a13.38 13.38 0 00-7 0C6.27.65 5.09 1 5.09 1A5.06 5.06 0 005 4.77a5.04 5.04 0 00-1.5 3.78c0 5.42 3.3 6.61 6.44 7A3.37 3.37 0 009 18.13V22"/></svg>
          <span class="contact-label">GitHub</span>
          <a href="https://github.com/qyyyy09315" class="contact-value">github.com/qyyyy09315</a>
        </div>
        <div class="contact-item">
          <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M21 10c0 7-9 13-9 13s-9-6-9-13a9 9 0 0118 0z"/><circle cx="12" cy="10" r="3"/></svg>
          <span class="contact-label">所在单位</span>
          <span class="contact-value">大连海洋大学 信息工程学院 大数据系</span>
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

.emails-list {
  display: flex;
  flex-direction: column;
  gap: .75rem;
  margin-bottom: 2rem;
  position: relative;
}

.email-card {
  display: flex;
  align-items: flex-start;
  gap: .75rem;
  padding: 1rem;
  background: var(--bg-subtle);
  border-radius: 10px;
}

.email-icon {
  color: var(--text-muted);
  flex-shrink: 0;
  margin-top: .125rem;
}

.email-info {
  display: flex;
  flex-direction: column;
  gap: .25rem;
}

.email-type {
  font-family: var(--font-mono);
  font-size: var(--text-sm);
  color: var(--accent);
  font-weight: 500;
  text-transform: uppercase;
  letter-spacing: .05em;
}

.email-addr {
  font-size: var(--text-base);
  font-weight: 600;
  color: var(--text);
  text-decoration: none;
  word-break: break-all;
}

.email-addr:hover {
  color: var(--accent);
}

.email-note {
  font-size: var(--text-xs);
  color: var(--text-muted);
}

.contact-row {
  display: flex;
  gap: 2rem;
  flex-wrap: wrap;
}

.contact-item {
  display: flex;
  align-items: center;
  gap: .5rem;
  font-size: var(--text-sm);
}

.contact-item svg {
  color: var(--text-muted);
  flex-shrink: 0;
}

.contact-label {
  font-family: var(--font-mono);
  color: var(--text-muted);
  text-transform: uppercase;
  letter-spacing: .05em;
}

.contact-value {
  color: var(--text);
  font-weight: 500;
  text-decoration: none;
}

.contact-value:hover {
  color: var(--accent);
}

@media (max-width: 768px) {
  .section { padding: 3rem 1.25rem; justify-content: flex-start; }

  .email-card { padding: .875rem; }

  .contact-row {
    flex-direction: column;
    gap: 1rem;
  }

  .decor-blob { opacity: 0.25; }
}
</style>
