<script setup>
import Header from './components/Header.vue'
import Footer from './components/Footer.vue'
import AgeVerification from './components/AgeVerification.vue'
</script>

<template>
  <AgeVerification />
  <Header />
  <main>
    <router-view v-slot="{ Component }">
      <transition name="fade" mode="out-in">
        <component :is="Component" />
      </transition>
    </router-view>
  </main>
  <Footer />
</template>

<style scoped>
main {
  width: 100%;
  min-height: calc(100vh - 160px); /* Adjust for header and footer */
  padding-top: 80px; /* Space for fixed header */
}

/* Page Transitions */
.fade-enter-active,
.fade-leave-active {
  transition: opacity var(--transition-normal), transform var(--transition-normal);
}

.fade-enter-from,
.fade-leave-to {
  opacity: 0;
  transform: translateY(10px);
}
</style>
