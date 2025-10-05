<script setup lang="ts">
// TheHeader.vue - Top navigation component
</script>

<template>
  <header class="header">
    <div class="container">
      <div class="logo-container">
        <img src="/logo.jpg" alt="S&G Homewatch Logo" class="logo">
        <div class="logo-text">
          <h1>S&G Homewatch</h1>
        </div>
      </div>
      <nav class="nav-links">
        <a href="#home">Home</a>
        <a href="#services">Services</a>
        <a href="#about">About</a>
        <a href="#contact">Contact</a>
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
}

@media (max-width: 768px) {
  .logo-text {
    display: none;
  }
}
</style>
