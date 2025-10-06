<script setup lang="ts">
import { ref } from 'vue';
// TheHeader.vue - Top navigation component

const mobileMenuOpen = ref(false);

const toggleMobileMenu = () => {
  mobileMenuOpen.value = !mobileMenuOpen.value;
};

const closeMenu = () => {
  mobileMenuOpen.value = false;
};
</script>

<template>
  <header class="header">
    <div class="container">
      <div class="logo-container">
        <a href="#home">
          <img src="/logo.jpg" alt="S&G Homewatch Logo" class="logo">
        </a>
        <div class="logo-text">
          <h1>S&G Homewatch</h1>
        </div>
      </div>
      
      <!-- Mobile menu toggle button -->
      <button 
        class="mobile-menu-toggle" 
        @click="toggleMobileMenu" 
        aria-label="Toggle menu"
        :class="{ 'is-active': mobileMenuOpen }"
      >
        <span></span>
        <span></span>
        <span></span>
      </button>
      
      <!-- Desktop navigation -->
      <nav class="nav-links desktop-nav">
        <a href="#home">Home</a>
        <a href="#services">Services</a>
        <a href="#about">About</a>
        <a href="#contact">Contact</a>
      </nav>
      
      <!-- Mobile navigation -->
      <nav class="mobile-nav" :class="{ 'is-open': mobileMenuOpen }">
        <a href="#home" @click="closeMenu">Home</a>
        <a href="#services" @click="closeMenu">Services</a>
        <a href="#about" @click="closeMenu">About</a>
        <a href="#contact" @click="closeMenu">Contact</a>
      </nav>
    </div>
  </header>
</template>

<style scoped>
.logo {
  width: 50px;
  height: 50px;
  border-radius: 8px;
  margin-right: 1rem;
  object-fit: cover;
}

.logo-text h1 {
  margin: 0;
  font-size: 1.5rem;
  color: var(--primary-color);
}

.container {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 0.8rem 1rem;
  box-sizing: border-box;
  width: 100%;
}

.logo-container {
  display: flex;
  align-items: center;
}

.nav-links a {
  margin: 0 0.8rem;
  font-weight: 600;
  text-decoration: none;
  color: var(--text-color);
  transition: color 0.3s ease;
}

.nav-links a:hover {
  color: var(--primary-color);
}

.mobile-nav {
  display: none;
  position: absolute;
  top: 100%;
  left: 0;
  right: 0;
  background: var(--white);
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  padding: 0.5rem;
  flex-direction: column;
  transform: translateY(-20px);
  opacity: 0;
  transition: transform 0.3s ease, opacity 0.3s ease;
  z-index: 99;
  pointer-events: none; /* Ignore clicks when hidden */
}

.mobile-nav.is-open {
  transform: translateY(0);
  opacity: 1;
  pointer-events: auto; /* Accept clicks when visible */
}

.mobile-nav a {
  padding: 0.8rem;
  text-align: center;
  font-size: 1.1rem;
  border-bottom: 1px solid var(--light-gray);
}

.mobile-nav a:last-child {
  border-bottom: none;
}

.mobile-menu-toggle {
  display: none;
  background: transparent;
  border: none;
  width: 24px; /* Make it smaller */
  height: 24px;
  padding: 0;
  cursor: pointer;
  position: relative;
  z-index: 100;
  margin-right: 10px; /* Add more margin to keep it from the edge */
}

.mobile-menu-toggle span {
  display: block;
  width: 100%;
  height: 2px; /* Thinner lines */
  background-color: var(--primary-color);
  margin: 4px 0;
  transition: 0.3s;
  border-radius: 2px;
}

/* Fix the animation for the hamburger menu */
.mobile-menu-toggle.is-active span:nth-child(1) {
  transform: rotate(-45deg) translate(-4px, 4px);
}

.mobile-menu-toggle.is-active span:nth-child(2) {
  opacity: 0;
}

.mobile-menu-toggle.is-active span:nth-child(3) {
  transform: rotate(45deg) translate(-4px, -4px);
}

@media (max-width: 768px) {
  .logo-text {
    display: none;
  }
  
  .desktop-nav {
    display: none;
  }
  
  .mobile-menu-toggle {
    display: block;
  }
  
  .mobile-nav {
    display: flex;
  }
  
  .container {
    padding: 0.6rem 0.8rem;
    flex-wrap: nowrap; /* Prevent wrapping of flex items */
    align-items: center;
  }
  
  /* Ensure the header is properly constrained */
  .header {
    width: 100%;
    box-sizing: border-box;
    overflow: visible; /* Changed to visible so the dropdown menu can show */
    position: relative;
  }
  
  .header .container {
    padding: 0.6rem 0.8rem;
  }
  
  /* Make logo smaller on mobile */
  .logo {
    width: 40px;
    height: 40px;
    margin-right: 0.5rem;
  }
}
</style>
