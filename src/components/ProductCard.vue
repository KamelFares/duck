<script setup>
defineProps({
  product: {
    type: Object,
    required: true
  }
})
</script>

<template>
  <div class="product-card glass">
    <div class="card-image-container">
      <img :src="product.image" :alt="product.name" class="card-image" />
    </div>
    <div class="card-content">
      <div class="card-header">
        <h3 class="card-title">{{ product.name }}</h3>
        <span class="card-price">€{{ product.price }}</span>
      </div>
      <p class="card-description">{{ product.description }}</p>
      <div class="card-footer">
        <button class="btn btn-outline w-full">Add to Cart</button>
      </div>
    </div>
  </div>
</template>

<style scoped>
.product-card {
  border-radius: var(--radius-md);
  overflow: hidden;
  transition: all var(--transition-normal);
  display: flex;
  flex-direction: column;
  height: 100%;
}

.product-card:hover {
  transform: translateY(-8px);
  box-shadow: var(--shadow-glow);
  border-color: rgba(212, 175, 55, 0.5);
}

.card-image-container {
  height: 280px;
  background: radial-gradient(circle at center, rgba(255,255,255,0.05) 0%, transparent 70%);
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 24px;
  position: relative;
  overflow: hidden;
}

.card-image {
  max-height: 100%;
  object-fit: contain;
  transition: transform var(--transition-normal);
  filter: drop-shadow(0 10px 15px rgba(0,0,0,0.5));
}

.product-card:hover .card-image {
  transform: scale(1.05);
}

.card-content {
  padding: 24px;
  display: flex;
  flex-direction: column;
  flex-grow: 1;
}

.card-header {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  margin-bottom: 12px;
}

.card-title {
  font-size: 1.5rem;
  color: var(--color-text-primary);
}

.card-price {
  font-size: 1.25rem;
  font-weight: 600;
  color: var(--color-accent-primary);
}

.card-description {
  font-size: 0.95rem;
  line-height: 1.5;
  margin-bottom: 24px;
  flex-grow: 1;
}

.w-full {
  width: 100%;
}
</style>
