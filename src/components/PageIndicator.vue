<template>
  <div class="page-indicator">
    <button
      v-for="index in total"
      :key="index"
      :class="['indicator-dot', { active: index - 1 === current }]"
      @click="$emit('select', index - 1)"
      :aria-label="`Go to page ${index}`"
    >
      <span class="dot-inner"></span>
      <span class="dot-label">{{ labels[index - 1] }}</span>
    </button>
  </div>
</template>

<script setup>
defineProps({
  total: { type: Number, required: true },
  current: { type: Number, required: true }
})
defineEmits(['select'])

const labels = ['Home', 'About', 'Skills', 'Edu', 'Contact', 'Footer']
</script>

<style scoped>
.page-indicator {
  position: fixed;
  right: 2rem;
  top: 50%;
  transform: translateY(-50%);
  display: flex;
  flex-direction: column;
  gap: 0.5rem;
  z-index: 50;
}

.indicator-dot {
  display: flex;
  align-items: center;
  gap: 0.75rem;
  background: none;
  border: none;
  cursor: pointer;
  padding: 0.375rem 0;
  position: relative;
}

.dot-inner {
  width: 8px;
  height: 8px;
  border-radius: 50%;
  background: var(--border);
  transition: all var(--duration-normal) var(--ease-out);
  flex-shrink: 0;
}

.indicator-dot:hover .dot-inner {
  background: var(--text-muted);
  transform: scale(1.2);
}

.indicator-dot.active .dot-inner {
  background: var(--accent);
  transform: scale(1.3);
}

.dot-label {
  font-family: var(--font-mono);
  font-size: 0.6875rem;
  color: var(--text-muted);
  opacity: 0;
  transform: translateX(8px);
  transition: all var(--duration-normal) var(--ease-out);
  white-space: nowrap;
  pointer-events: none;
}

.indicator-dot:hover .dot-label,
.indicator-dot.active .dot-label {
  opacity: 1;
  transform: translateX(0);
}

@media (max-width: 768px) {
  .page-indicator {
    right: 1rem;
  }

  .dot-label {
    display: none;
  }
}
</style>
