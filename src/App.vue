<script setup>
import Header from './components/Header.vue'
import Hero from './components/Hero.vue'
import ProductList from './components/ProductList.vue'
import Footer from './components/Footer.vue'
import AgeVerification from './components/AgeVerification.vue'
</script>

<template>
  <AgeVerification />
  <Header />
  <main>
    <Hero />
    <ProductList />
  </main>
  <Footer />
</template>

<style scoped>
main {
  width: 100%;
}
</style>
