<template>
  <nav class="navbar">
    <div class="nav-container">
      <a href="#" class="nav-logo" @click.prevent="$emit('navigate', 0)">Yue-xin G.</a>
      <ul class="nav-links">
        <li><a href="#about" :class="{ active: currentSection === 1 }" @click.prevent="$emit('navigate', 1)">关于</a></li>
        <li><a href="#skills" :class="{ active: currentSection === 2 }" @click.prevent="$emit('navigate', 2)">技能</a></li>
        <li><a href="#education" :class="{ active: currentSection === 3 }" @click.prevent="$emit('navigate', 3)">教育</a></li>
        <li><a href="#contact" :class="{ active: currentSection === 4 }" @click.prevent="$emit('navigate', 4)">联系</a></li>
      </ul>
    </div>
  </nav>
</template>

<script setup>
defineProps({
  currentSection: { type: Number, default: 0 }
})
defineEmits(['navigate'])
</script>

<style scoped>
.navbar {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  background: rgba(255, 255, 255, 0.92);
  backdrop-filter: blur(12px);
  border-bottom: 1px solid #e5e7eb;
  z-index: 100;
}

.nav-container {
  max-width: 960px;
  margin: 0 auto;
  padding: 0 2rem;
  height: 60px;
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.nav-logo {
  font-weight: 600;
  font-size: 1rem;
  color: #1a1a1a;
  text-decoration: none;
}

.nav-links {
  display: flex;
  gap: 2rem;
  list-style: none;
  margin: 0;
  padding: 0;
}

.nav-links a {
  color: #6b7280;
  text-decoration: none;
  font-size: 0.875rem;
  transition: color 0.2s;
}

.nav-links a:hover,
.nav-links a.active {
  color: #2563eb;
}

@media (max-width: 640px) {
  .nav-links {
    display: none;
  }
}
</style>