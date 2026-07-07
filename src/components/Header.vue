<script setup>
</script>

<template>
  <header class="header glass">
    <div class="container header-content">
      <div class="logo">
        <span class="text-gradient">Quack</span>Spirits
      </div>
      <nav class="nav">
        <a href="#boxes">Our Boxes</a>
        <a href="#about">About</a>
        <a href="#faq">FAQ</a>
      </nav>
      <div class="actions">
        <button class="btn btn-primary cart-btn">
          <span>Cart</span>
          <div class="cart-badge">0</div>
        </button>
      </div>
    </div>
  </header>
</template>

<style scoped>
.header {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  z-index: 100;
  padding: 16px 0;
  border-bottom: var(--border-subtle);
}

.header-content {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.logo {
  font-size: 1.5rem;
  font-weight: 700;
  letter-spacing: -0.05em;
  color: var(--color-text-primary);
}

.nav {
  display: flex;
  gap: 32px;
}

.nav a {
  font-weight: 500;
  color: var(--color-text-secondary);
  position: relative;
}

.nav a:hover {
  color: var(--color-accent-primary);
}

.nav a::after {
  content: '';
  position: absolute;
  width: 0;
  height: 2px;
  bottom: -4px;
  left: 0;
  background-color: var(--color-accent-primary);
  transition: width var(--transition-normal);
}

.nav a:hover::after {
  width: 100%;
}

.cart-btn {
  display: flex;
  gap: 8px;
  padding: 8px 16px;
  border-radius: 20px;
}

.cart-badge {
  background: var(--color-bg-base);
  color: var(--color-accent-primary);
  border-radius: 50%;
  width: 24px;
  height: 24px;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 0.8rem;
  font-weight: 700;
}
</style>
