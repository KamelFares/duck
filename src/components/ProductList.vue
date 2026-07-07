<script setup>
import { ref } from 'vue'
import ProductCard from './ProductCard.vue'

const products = ref([
  {
    id: 1,
    name: 'Standard Duck Box',
    price: 15.99,
    description: 'A curated selection of everyday premium spirits. Perfect for casual evenings and discovering new favorites. Contains 2-3 bottles.',
    image: '/standard_duck_box.png'
  },
  {
    id: 2,
    name: 'Premium Duck Box',
    price: 49.99,
    description: 'Elevate your collection with top-shelf selections. Includes rare finds and aged spirits. Contains 3-4 bottles of exceptional quality.',
    image: '/premium_duck_box.png'
  },
  {
    id: 3,
    name: 'Luxury Golden Duck Box',
    price: 149.99,
    description: 'The ultimate indulgence. Ultra-rare, limited edition, and highly sought-after bottles. A once-in-a-lifetime unboxing experience.',
    image: '/luxury_duck_box.png'
  }
])
</script>

<template>
  <section id="boxes" class="products-section">
    <div class="container">
      <div class="section-header">
        <h2 class="section-title">Curated <span class="text-gradient">Collections</span></h2>
        <p class="section-subtitle">Choose your level of LuckyDuck. Each box is guaranteed to exceed its retail value.</p>
      </div>
      
      <div class="products-grid">
        <ProductCard 
          v-for="product in products" 
          :key="product.id" 
          :product="product" 
        />
      </div>
    </div>
  </section>
</template>

<style scoped>
.products-section {
  padding: 100px 0;
  background-color: var(--color-bg-base);
  position: relative;
}

.section-header {
  text-align: center;
  margin-bottom: 64px;
}

.section-title {
  font-size: 3rem;
  margin-bottom: 16px;
}

.section-subtitle {
  font-size: 1.1rem;
  max-width: 600px;
  margin: 0 auto;
}

.products-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
  gap: 32px;
}
</style>
