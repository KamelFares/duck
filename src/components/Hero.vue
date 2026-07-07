<script setup>
</script>

<template>
  <section class="hero">
    <div class="hero-bg"></div>
    <div class="container hero-content">
      <div class="hero-text">
        <h1 class="hero-title">Unbox the <span class="text-gradient">Extraordinary</span></h1>
        <p class="hero-subtitle">Discover curated collections of premium and luxury . Every box is a carefully crafted surprise, designed for the sophisticated palate.</p>
        <div class="hero-actions">
          <a href="#boxes" class="btn btn-primary hero-btn">Explore Collections</a>
        </div>
      </div>
      <div class="hero-image-wrapper">
        <div class="glow-effect"></div>
        <img src="/hero_duck_box.png" alt="Premium Mystery Duck Box" class="hero-image" />
      </div>
    </div>
  </section>
</template>

<style scoped>
.hero {
  position: relative;
  min-height: 100vh;
  display: flex;
  align-items: center;
  padding-top: 80px; /* Space for header */
  overflow: hidden;
}

.hero-bg {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: radial-gradient(circle at 70% 50%, rgba(212, 175, 55, 0.08) 0%, rgba(15, 15, 17, 1) 60%);
  z-index: -1;
}

.hero-content {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 48px;
  align-items: center;
}

.hero-title {
  font-size: 4.5rem;
  line-height: 1.1;
  margin-bottom: 24px;
}

.hero-subtitle {
  font-size: 1.25rem;
  line-height: 1.6;
  margin-bottom: 40px;
  max-width: 90%;
}

.hero-btn {
  font-size: 1.1rem;
  padding: 16px 32px;
}

.hero-image-wrapper {
  position: relative;
  display: flex;
  justify-content: center;
  align-items: center;
}

.glow-effect {
  position: absolute;
  width: 300px;
  height: 300px;
  background: var(--color-accent-primary);
  filter: blur(120px);
  opacity: 0.15;
  border-radius: 50%;
  z-index: -1;
  animation: pulse 4s ease-in-out infinite alternate;
}

.hero-image {
  max-width: 120%;
  height: auto;
  transform: translateY(0);
  animation: float 6s ease-in-out infinite;
  filter: drop-shadow(0 20px 30px rgba(0,0,0,0.5));
}

@keyframes float {
  0% { transform: translateY(0px); }
  50% { transform: translateY(-20px); }
  100% { transform: translateY(0px); }
}

@keyframes pulse {
  0% { opacity: 0.1; transform: scale(1); }
  100% { opacity: 0.25; transform: scale(1.1); }
}

@media (max-width: 992px) {
  .hero-content {
    grid-template-columns: 1fr;
    text-align: center;
    gap: 32px;
  }
  
  .hero-subtitle {
    margin: 0 auto 32px;
  }
  
  .hero-title {
    font-size: 3.5rem;
  }
}
</style>
