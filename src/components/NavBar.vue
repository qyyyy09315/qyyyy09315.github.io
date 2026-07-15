<template>
  <nav class="navbar">
    <div class="nav-inner">
      <div class="nav-left">
        <a href="#" class="nav-logo" @click.prevent="$emit('navigate', 0)">
          Yue-xin G.
        </a>
        <ul class="nav-links">
          <li v-for="(link, idx) in links" :key="idx">
            <a
              :href="link.href"
              :class="{ active: currentSection === link.index }"
              @click.prevent="$emit('navigate', link.index)"
            >
              {{ link.label }}
            </a>
          </li>
        </ul>
      </div>
    </div>
  </nav>
</template>

<script setup>
defineProps({
  currentSection: { type: Number, default: 0 }
})
defineEmits(['navigate'])

const links = [
  { label: '关于', href: '#about', index: 1 },
  { label: '技能', href: '#skills', index: 2 },
  { label: '项目', href: '#projects', index: 3 },
  { label: '教育', href: '#education', index: 4 },
  { label: '联系', href: '#contact', index: 5 }
]
</script>

<style scoped>
.navbar {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  z-index: 100;
  background: rgba(251, 251, 250, .82);
  backdrop-filter: blur(12px);
  border-bottom: 1px solid var(--border-subtle);
}

.nav-inner {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 2rem;
  height: 56px;
  display: flex;
  align-items: center;
}

.nav-left {
  display: flex;
  align-items: center;
  gap: 2rem;
}

.nav-logo {
  font-family: var(--font-mono);
  font-size: var(--text-sm);
  font-weight: 500;
  color: var(--text);
  text-decoration: none;
  letter-spacing: -.01em;
  white-space: nowrap;
}

.nav-links {
  display: flex;
  gap: 1.5rem;
  list-style: none;
  margin: 0;
  padding: 0;
}

.nav-links a {
  color: var(--text-muted);
  text-decoration: none;
  font-size: var(--text-sm);
  font-weight: 400;
  transition: color var(--duration-fast) var(--ease-out);
  white-space: nowrap;
}

.nav-links a:hover {
  color: var(--text);
}

.nav-links a.active {
  color: var(--accent);
}

@media (max-width: 640px) {
  .nav-inner {
    padding: 0 1.25rem;
    height: 48px;
  }

  .nav-left {
    gap: 1.25rem;
    overflow-x: auto;
  }

  .nav-links {
    gap: 1rem;
  }

  .nav-links a {
    font-size: var(--text-xs);
  }

  .nav-logo {
    font-size: var(--text-xs);
  }
}
</style>
