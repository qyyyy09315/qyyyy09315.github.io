<template>
  <div class="page-indicator">
    <button
      v-for="index in total"
      :key="index"
      :class="['dot', { active: index - 1 === current }]"
      @click="$emit('select', index - 1)"
      :aria-label="`Go to page ${index}`"
    />
  </div>
</template>

<script setup>
defineProps({
  total: { type: Number, required: true },
  current: { type: Number, required: true }
})
defineEmits(['select'])
</script>

<style scoped>
.page-indicator {
  position: fixed;
  right: 2rem;
  top: 50%;
  transform: translateY(-50%);
  display: flex;
  flex-direction: column;
  gap: 0.75rem;
  z-index: 50;
}

.dot {
  width: 10px;
  height: 10px;
  border-radius: 50%;
  background: #d1d5db;
  border: none;
  cursor: pointer;
  transition: all 0.3s;
  padding: 0;
}

.dot:hover {
  background: #9ca3af;
}

.dot.active {
  background: #2563eb;
  transform: scale(1.3);
}

@media (max-width: 640px) {
  .page-indicator {
    right: 1rem;
  }
}
</style>