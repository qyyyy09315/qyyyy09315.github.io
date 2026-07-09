<template>
  <div class="page-indicator">
    <button
      v-for="(label, index) in labels"
      :key="index"
      :class="['dot', { active: index === current }]"
      :aria-label="`前往第 ${index + 1} 页`"
      @click="$emit('select', index)"
    >
      <span class="dot-number">{{ String(index + 1).padStart(2, '0') }}</span>
      <span class="dot-label">{{ label }}</span>
    </button>
  </div>
</template>

<script setup>
defineProps({
  current: { type: Number, required: true },
  total: { type: Number, required: true }
})
defineEmits(['select'])

const labels = ['首页', '关于', '技能', '教育', '联系', '页脚']
</script>

<style scoped>
.page-indicator {
  position: fixed;
  right: 2rem;
  top: 50%;
  transform: translateY(-50%);
  display: flex;
  flex-direction: column;
  gap: 1.25rem;
  z-index: 50;
}

.dot {
  display: flex;
  align-items: center;
  gap: 0.75rem;
  background: none;
  border: none;
  cursor: pointer;
  padding: 0;
  transition: all 250ms cubic-bezier(0.16, 1, 0.3, 1);
}

.dot-number {
  font-family: var(--font-mono);
  font-size: 0.6875rem;
  color: var(--text-muted);
  opacity: 0.6;
  transition: all 250ms cubic-bezier(0.16, 1, 0.3, 1);
}

.dot-label {
  font-size: 0.8125rem;
  color: var(--text-muted);
  opacity: 0;
  transform: translateX(8px);
  transition: all 250ms cubic-bezier(0.16, 1, 0.3, 1);
  white-space: nowrap;
}

.dot:hover .dot-label,
.dot.active .dot-label {
  opacity: 1;
  transform: translateX(0);
}

.dot:hover .dot-number,
.dot.active .dot-number {
  opacity: 1;
  color: var(--accent);
}

.dot.active {
  transform: scale(1.05);
}

@media (max-width: 768px) {
  .page-indicator {
    right: 1rem;
    gap: 1rem;
  }
  .dot-label {
    display: none;
  }
}
</style>