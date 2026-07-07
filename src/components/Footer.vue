<script setup>
</script>

<template>
  <footer class="footer">
    <div class="container footer-content">
      <div class="footer-brand">
        <div class="logo">
          <span class="text-gradient">QuackSpirits</span>
        </div>
        <p class="footer-desc">Curated premium alcohol surprise boxes for the sophisticated connoisseur.</p>
      </div>
      
      <div class="footer-links">
        <div class="link-group">
          <h4>Shop</h4>
          <ul>
            <li><a href="#boxes">All Boxes</a></li>
            <li><a href="#">Gift Cards</a></li>
            <li><a href="#">Corporate Gifts</a></li>
          </ul>
        </div>
        
        <div class="link-group">
          <h4>Support</h4>
          <ul>
            <li><a href="#">FAQ</a></li>
            <li><a href="#">Shipping</a></li>
            <li><a href="#">Returns</a></li>
            <li><a href="#">Contact Us</a></li>
          </ul>
        </div>
        
        <div class="link-group">
          <h4>Legal</h4>
          <ul>
            <li><a href="#">Terms of Service</a></li>
            <li><a href="#">Privacy Policy</a></li>
            <li><a href="#">Age Verification</a></li>
          </ul>
        </div>
      </div>
    </div>
    <div class="footer-bottom">
      <div class="container">
        <p>&copy; 2026 QuackSpirits. All rights reserved. Must be 21+ to purchase.</p>
      </div>
    </div>
  </footer>
</template>

<style scoped>
.footer {
  background-color: var(--color-bg-surface);
  padding-top: 80px;
  border-top: var(--border-subtle);
}

.footer-content {
  display: grid;
  grid-template-columns: 1fr 2fr;
  gap: 64px;
  margin-bottom: 64px;
}

.logo {
  font-size: 1.5rem;
  font-weight: 700;
  margin-bottom: 16px;
}

.footer-desc {
  max-width: 300px;
}

.footer-links {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 32px;
}

.link-group h4 {
  font-size: 1.1rem;
  margin-bottom: 24px;
  color: var(--color-text-primary);
}

.link-group ul {
  list-style: none;
  padding: 0;
  margin: 0;
}

.link-group li {
  margin-bottom: 12px;
}

.link-group a {
  color: var(--color-text-secondary);
}

.link-group a:hover {
  color: var(--color-accent-primary);
}

.footer-bottom {
  border-top: var(--border-subtle);
  padding: 24px 0;
  text-align: center;
  background-color: var(--color-bg-base);
}

.footer-bottom p {
  font-size: 0.9rem;
}

@media (max-width: 768px) {
  .footer-content {
    grid-template-columns: 1fr;
    gap: 48px;
  }
  
  .footer-links {
    grid-template-columns: 1fr 1fr;
  }
}

@media (max-width: 480px) {
  .footer-links {
    grid-template-columns: 1fr;
  }
}
</style>
