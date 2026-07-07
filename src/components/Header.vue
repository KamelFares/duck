<script setup>
</script>

<template>
  <header class="header glass">
    <div class="container header-content">
      <router-link to="/" class="logo">
        <svg class="duck-icon" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
          <path d="M20,13c-0.2,0-0.3,0-0.4,0c-0.6-1.5-2.1-2.6-3.8-2.6c-0.5,0-0.9,0.1-1.3,0.3c0-0.2-0.1-0.4-0.1-0.6c0-2-1.6-3.6-3.6-3.6 s-3.6,1.6-3.6,3.6c0,0.4,0.1,0.8,0.2,1.2C5.9,12,5,13.4,5,15c0,1.3,0.8,2.4,1.9,2.8C7.4,18.5,8.1,19,9,19c1.6,0,3-1.1,3.4-2.6 c0.3,0.1,0.7,0.1,1,0.1c1.3,0,2.5-0.7,3.1-1.8c0.5,0.2,1,0.3,1.5,0.3c2.2,0,4-1.8,4-4S22.2,13,20,13z M10.8,9.5 c0.5,0,0.9,0.4,0.9,0.9s-0.4,0.9-0.9,0.9s-0.9-0.4-0.9-0.9S10.3,9.5,10.8,9.5z M4,13.5C3.4,13.5,3,13,3,12.5S3.4,11.5,4,11.5 s1,0.4,1,0.9S4.6,13.5,4,13.5z" />
        </svg>
        <span class="text-gradient">Lucky</span>Duck
      </router-link>
      <nav class="nav">
        <router-link to="/boxes">Our Boxes</router-link>
        <router-link to="/about">About</router-link>
        <router-link to="/faq">FAQ</router-link>
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
  display: flex;
  align-items: center;
  gap: 8px;
  font-size: 1.5rem;
  font-weight: 700;
  letter-spacing: -0.05em;
  color: var(--color-text-primary);
}

.duck-icon {
  width: 24px;
  height: 24px;
  fill: var(--color-accent-primary);
  filter: drop-shadow(0 0 5px var(--color-accent-glow));
}

.nav {
  display: flex;
  gap: 32px;
}

.nav a {
  font-weight: 500;
  color: var(--color-text-secondary);
  position: relative;
  transition: color var(--transition-normal);
}

.nav a:hover,
.nav a.router-link-active {
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

.nav a:hover::after,
.nav a.router-link-active::after {
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
