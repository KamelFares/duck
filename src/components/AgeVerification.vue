<script setup>
import { ref, onMounted } from 'vue'

const isVerified = ref(true)
const isRejected = ref(false)

onMounted(() => {
  const verified = localStorage.getItem('age_verified')
  if (!verified) {
    isVerified.value = false
  }
})

const verifyAge = () => {
  localStorage.setItem('age_verified', 'true')
  isVerified.value = true
}

const rejectAge = () => {
  isRejected.value = true
}
</script>

<template>
  <div v-if="!isVerified" class="age-modal-overlay">
    <div class="age-modal glass">
      <div v-if="!isRejected" class="age-content">
        <h2 class="age-title">Age Verification</h2>
        <p class="age-desc">You must be 18 or older to view and purchase our premium alcohol surprise boxes.</p>
        <p class="age-question">Are you over 18?</p>
        <div class="age-actions">
          <button @click="verifyAge" class="btn btn-primary">Yes, I am over 18</button>
          <button @click="rejectAge" class="btn btn-outline">No, I am under 18</button>
        </div>
      </div>
      <div v-else class="age-content">
        <h2 class="age-title text-gradient">Access Denied</h2>
        <p class="age-desc">Sorry, you must be 18 or older to enter this site. Please return when you are of legal drinking age.</p>
      </div>
    </div>
  </div>
</template>

<style scoped>
.age-modal-overlay {
  position: fixed;
  top: 0;
  left: 0;
  width: 100vw;
  height: 100vh;
  background: rgba(0, 0, 0, 0.85);
  backdrop-filter: blur(10px);
  z-index: 1000;
  display: flex;
  align-items: center;
  justify-content: center;
}

.age-modal {
  max-width: 500px;
  width: 90%;
  padding: 40px;
  border-radius: var(--radius-lg);
  text-align: center;
  box-shadow: var(--shadow-md), 0 0 40px rgba(212, 175, 55, 0.15);
  border: 1px solid rgba(212, 175, 55, 0.3);
  background: var(--color-bg-surface);
}

.age-title {
  font-size: 2rem;
  margin-bottom: 16px;
  color: var(--color-text-primary);
}

.age-desc {
  margin-bottom: 24px;
  font-size: 1.1rem;
}

.age-question {
  font-size: 1.3rem;
  font-weight: 600;
  margin-bottom: 32px;
  color: var(--color-accent-primary);
}

.age-actions {
  display: flex;
  flex-direction: column;
  gap: 16px;
}

.age-actions button {
  width: 100%;
}
</style>
