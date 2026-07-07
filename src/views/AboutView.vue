<script setup>
</script>

<template>
  <div class="about-page container">
    <div class="glass about-content">
      <h1 class="text-gradient">About Lucky Duck</h1>
      <p class="lead">We curate the world's most exclusive spirits, delivering premium surprise boxes right to your doorstep.</p>
      
      <div class="grid">
        <div class="feature">
          <div class="icon">✨</div>
          <h3>Premium Quality</h3>
          <p>Every bottle is hand-selected by our expert sommeliers, ensuring only the highest quality spirits make it into our boxes.</p>
        </div>
        <div class="feature">
          <div class="icon">🎁</div>
          <h3>The Surprise</h3>
          <p>The joy of unboxing is part of the experience. Each box contains a carefully guarded secret until it reaches your hands.</p>
        </div>
        <div class="feature">
          <div class="icon">🦆</div>
          <h3>The Lucky Duck</h3>
          <p>A symbol of good fortune and exceptional taste. Finding a rare vintage makes you a truly lucky duck.</p>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.about-page {
  padding-top: 40px;
  padding-bottom: 80px;
  animation: fadeIn var(--transition-slow);
}

.about-content {
  padding: 60px;
  border-radius: var(--radius-lg);
  text-align: center;
}

.about-content h1 {
  font-size: 3.5rem;
  margin-bottom: 24px;
}

.lead {
  font-size: 1.25rem;
  max-width: 700px;
  margin: 0 auto 60px;
  color: var(--color-text-primary);
}

.grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 40px;
  text-align: left;
}

.feature {
  padding: 30px;
  background: rgba(255, 255, 255, 0.03);
  border-radius: var(--radius-md);
  border: 1px solid rgba(255, 255, 255, 0.05);
  transition: transform var(--transition-normal), box-shadow var(--transition-normal);
}

.feature:hover {
  transform: translateY(-5px);
  box-shadow: 0 10px 30px rgba(0, 0, 0, 0.5);
  border-color: rgba(212, 175, 55, 0.2);
}

.icon {
  font-size: 2.5rem;
  margin-bottom: 16px;
}

.feature h3 {
  font-size: 1.5rem;
  margin-bottom: 12px;
  color: var(--color-accent-primary);
}

@keyframes fadeIn {
  from { opacity: 0; }
  to { opacity: 1; }
}

@media (max-width: 768px) {
  .about-content {
    padding: 30px;
  }
}
</style>
