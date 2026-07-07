<script setup>
</script>

<template>
  <div class="faq-page container">
    <div class="page-header">
      <h1 class="text-gradient">Frequently Asked Questions</h1>
      <p>Everything you need to know about our Lucky Duck boxes.</p>
    </div>
    
    <div class="faq-list glass">
      <div class="faq-item">
        <h3>What is in a Lucky Duck box?</h3>
        <p>Each box contains a premium, full-sized bottle of luxury alcohol (whiskey, rum, tequila, etc.), carefully selected by our experts. The exact contents are a surprise until you open it!</p>
      </div>
      <div class="faq-item">
        <h3>How much does shipping cost?</h3>
        <p>We offer free standard shipping on all orders within the continental US. Expedited shipping options are available at checkout.</p>
      </div>
      <div class="faq-item">
        <h3>Can I choose the type of alcohol?</h3>
        <p>While the exact bottle is a surprise, we offer themed boxes (e.g., The Whiskey Box, The Tequila Box) so you can choose your preferred category.</p>
      </div>
      <div class="faq-item">
        <h3>Do I need to be 21+ to order?</h3>
        <p>Yes. By law, you must be at least 21 years of age to purchase and receive alcohol. An adult signature and ID verification are required upon delivery.</p>
      </div>
    </div>
  </div>
</template>

<style scoped>
.faq-page {
  padding-top: 40px;
  padding-bottom: 80px;
  max-width: 800px;
  animation: slideUp var(--transition-slow);
}

.page-header {
  text-align: center;
  margin-bottom: 40px;
}

.page-header h1 {
  font-size: 2.5rem;
  margin-bottom: 16px;
}

.faq-list {
  border-radius: var(--radius-lg);
  padding: 40px;
}

.faq-item {
  padding-bottom: 30px;
  margin-bottom: 30px;
  border-bottom: 1px solid rgba(255, 255, 255, 0.05);
}

.faq-item:last-child {
  padding-bottom: 0;
  margin-bottom: 0;
  border-bottom: none;
}

.faq-item h3 {
  font-size: 1.3rem;
  color: var(--color-accent-primary);
  margin-bottom: 12px;
}

.faq-item p {
  font-size: 1.1rem;
  line-height: 1.6;
}

@keyframes slideUp {
  from { 
    opacity: 0;
    transform: translateY(20px);
  }
  to { 
    opacity: 1;
    transform: translateY(0);
  }
}
</style>
