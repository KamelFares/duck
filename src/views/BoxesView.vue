<script setup>
import ProductList from '../components/ProductList.vue'
</script>

<template>
  <div class="boxes-page container">
    <div class="page-header">
      <h1 class="text-gradient">Our Exclusive Boxes</h1>
      <p>Discover the finest curated selections in our Lucky Duck boxes.</p>
    </div>
    <ProductList />
  </div>
</template>

<style scoped>
.boxes-page {
  padding-top: 40px;
  padding-bottom: 80px;
  animation: slideUp var(--transition-slow);
}

.page-header {
  text-align: center;
  margin-bottom: 60px;
}

.page-header h1 {
  font-size: 3rem;
  margin-bottom: 16px;
}

.page-header p {
  font-size: 1.2rem;
  max-width: 600px;
  margin: 0 auto;
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
