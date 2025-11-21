<script setup>
import { ref, onMounted, onUnmounted } from 'vue';

const isScrolled = ref(false);
const isMenuOpen = ref(false);

const handleScroll = () => {
  isScrolled.value = window.scrollY > 50;
};

const toggleMenu = () => {
  isMenuOpen.value = !isMenuOpen.value;
};

onMounted(() => {
  window.addEventListener('scroll', handleScroll);
});

onUnmounted(() => {
  window.removeEventListener('scroll', handleScroll);
});
</script>

<template>
  <nav :class="['navbar', { 'scrolled': isScrolled }]">
    <div class="container nav-content">
      <div class="logo">
        <span class="logo-text">Estudio<span class="highlight">Contable</span></span>
      </div>
      
      <button class="menu-toggle" @click="toggleMenu" aria-label="Toggle navigation">
        <span class="bar"></span>
        <span class="bar"></span>
        <span class="bar"></span>
      </button>

      <ul :class="['nav-links', { 'active': isMenuOpen }]">
        <li><a href="#home" @click="isMenuOpen = false">Inicio</a></li>
        <li><a href="#about" @click="isMenuOpen = false">Quiénes Somos</a></li>
        <li><a href="#services" @click="isMenuOpen = false">Servicios</a></li>
        <li><a href="#contact" @click="isMenuOpen = false" class="btn-contact">Contacto</a></li>
      </ul>
    </div>
  </nav>
</template>

<style scoped src="../styles/navbar.css"></style>
