<template>
  <footer class="footer">
    <p>&copy; {{ currentYear }} Yue-xin G. · Built with Vue 3 + Vite</p>
  </footer>
</template>

<script setup>
import { ref } from 'vue'

const currentYear = ref(new Date().getFullYear())
</script>

<style scoped>
.footer {
  border-top: 1px solid #e5e7eb;
  padding: 2rem 0;
  text-align: center;
}

.footer p {
  font-size: 0.8125rem;
  color: #6b7280;
}
</style>