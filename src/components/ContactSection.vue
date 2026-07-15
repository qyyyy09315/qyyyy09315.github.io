<template>
  <section id="contact" class="section">
    <div class="content">
      <div class="section-header">
        <div class="animate"><span class="section-label">04 / 联系</span></div>
        <h2 class="section-title animate animate-delay-1">联系方式</h2>
        <p class="section-subtitle animate animate-delay-2">
          欢迎通过以下方式联系
        </p>
      </div>

      <!-- 邮箱区：三个邮箱单独展示 -->
      <div class="emails-grid">
        <div class="card email-card animate animate-delay-2">
          <div class="email-header">
            <div class="contact-icon">
              <svg width="20" height="20" fill="none" stroke="currentColor" stroke-width="2"><path d="M4 4h16c1.1 0 2 .9 2 2v12c0 1.1-.9 2-2 2H4c-1.1 0-2-.9-2-2V6c0-1.1.9-2 2-2z"/><polyline points="22,6 12,13 2,6"/></svg>
            </div>
            <div class="email-info">
              <span class="email-type">工作 / 业务</span>
              <a href="mailto:gengyuexin@qq.com" class="email-addr">gengyuexin@qq.com</a>
            </div>
          </div>
          <span class="email-note">业务合作 / 工作机会</span>
        </div>

        <div class="card email-card animate animate-delay-3">
          <div class="email-header">
            <div class="contact-icon">
              <svg width="20" height="20" fill="none" stroke="currentColor" stroke-width="2"><path d="M4 4h16c1.1 0 2 .9 2 2v12c0 1.1-.9 2-2 2H4c-1.1 0-2-.9-2-2V6c0-1.1.9-2 2-2z"/><polyline points="22,6 12,13 2,6"/></svg>
            </div>
            <div class="email-info">
              <span class="email-type">日常</span>
              <a href="mailto:ykshboy@163.com" class="email-addr">ykshboy@163.com</a>
            </div>
          </div>
          <span class="email-note">日常使用，不经常查看</span>
        </div>

        <div class="card email-card animate animate-delay-4">
          <div class="email-header">
            <div class="contact-icon">
              <svg width="20" height="20" fill="none" stroke="currentColor" stroke-width="2"><path d="M4 4h16c1.1 0 2 .9 2 2v12c0 1.1-.9 2-2 2H4c-1.1 0-2-.9-2-2V6c0-1.1.9-2 2-2z"/><polyline points="22,6 12,13 2,6"/></svg>
            </div>
            <div class="email-info">
              <span class="email-type">Agent</span>
              <a href="mailto:qyyyy09315@agent.qq.com" class="email-addr">qyyyy09315@agent.qq.com</a>
            </div>
          </div>
          <span class="email-note">每天查看，日常使用</span>
        </div>
      </div>

      <!-- 其他联系方式 -->
      <div class="contact-grid">
        <div class="card contact-card animate animate-delay-4">
          <div class="contact-icon">
            <svg width="22" height="22" fill="none" stroke="currentColor" stroke-width="2"><path d="M9 19c-5 1.5-5-2.5-7-3m14 6v-3.87a3.37 3.37 0 00-.94-2.61c3.14-.35 6.44-1.54 6.44-7A5.04 5.04 0 0020 4.77 5.06 5.06 0 0019.91 1S18.73.65 16 2.48a13.38 13.38 0 00-7 0C6.27.65 5.09 1 5.09 1A5.06 5.06 0 005 4.77a5.04 5.04 0 00-1.5 3.78c0 5.42 3.3 6.61 6.44 7A3.37 3.37 0 009 18.13V22"/></svg>
          </div>
          <span class="contact-label">GitHub</span>
          <a href="https://github.com/qyyyy09315" class="contact-value">github.com/qyyyy09315</a>
        </div>

        <div class="card contact-card animate animate-delay-5">
          <div class="contact-icon">
            <svg width="22" height="22" fill="none" stroke="currentColor" stroke-width="2"><path d="M21 10c0 7-9 13-9 13s-9-6-9-13a9 9 0 0118 0z"/><circle cx="12" cy="10" r="3"/></svg>
          </div>
          <span class="contact-label">所在单位</span>
          <span class="contact-value">大连海洋大学<br>信息工程学院大数据系</span>
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

.section-header {
  margin-bottom: 2.5rem;
}

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

/* Emails grid */
.emails-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 1rem;
  margin-bottom: 2.5rem;
}

.email-card {
  display: flex;
  flex-direction: column;
  gap: .75rem;
  padding: 1.25rem;
}

.email-header {
  display: flex;
  align-items: center;
  gap: .75rem;
}

.email-info {
  display: flex;
  flex-direction: column;
  gap: 2px;
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
  font-size: var(--text-lg);
  font-weight: 600;
  color: var(--text);
  text-decoration: none;
  word-break: break-all;
}

.email-addr:hover {
  color: var(--accent);
}

.email-note {
  font-size: var(--text-sm);
  color: var(--text-muted);
  padding-left: 2.75rem; /* align with email address */
}

.contact-grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 1rem;
}

.contact-card {
  display: flex;
  flex-direction: column;
  gap: .5rem;
  padding: 1.25rem;
}

.contact-icon {
  width: 40px;
  height: 40px;
  border-radius: 10px;
  background: var(--accent-subtle);
  color: var(--accent);
  display: flex;
  align-items: center;
  justify-content: center;
  margin-bottom: .5rem;
}

.contact-label {
  font-size: var(--text-sm);
  color: var(--text-muted);
  font-family: var(--font-mono);
  text-transform: uppercase;
  letter-spacing: .05em;
}

.contact-value {
  font-size: var(--text-lg);
  font-weight: 600;
  color: var(--text);
  text-decoration: none;
  word-break: break-all;
  line-height: 1.5;
}

.contact-value:hover {
  color: var(--accent);
}

@media (max-width: 768px) {
  .section {
    padding: 4rem 1.25rem 3rem;
    justify-content: flex-start;
  }

  .emails-grid {
    grid-template-columns: 1fr;
    gap: .75rem;
    margin-bottom: 1.5rem;
  }

  .email-card {
    padding: 1rem;
  }

  .email-note {
    padding-left: 0;
  }

  .contact-grid {
    grid-template-columns: 1fr 1fr;
    gap: .75rem;
  }

  .contact-card {
    padding: 1rem;
  }

  .contact-icon {
    width: 36px;
    height: 36px;
  }

  .contact-value {
    font-size: var(--text-base);
  }
}
</style>