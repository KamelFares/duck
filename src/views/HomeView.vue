<script setup>
import Hero from '../components/Hero.vue'
</script>

<template>
  <div class="home">
    <Hero />
  </div>
</template>

<style scoped>
.home {
  animation: fadeIn var(--transition-slow);
}

@keyframes fadeIn {
  from { opacity: 0; }
  to { opacity: 1; }
}
</style>
