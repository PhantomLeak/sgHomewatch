<script setup lang="ts">
import TheHeader from './components/TheHeader.vue'
import TheFooter from './components/TheFooter.vue'
import HomePage from './components/HomePage.vue'
</script>

<template>
  <div class="app-container">
    <TheHeader />
    <main>
      <HomePage />
    </main>
    <TheFooter />
  </div>
</template>

<style scoped>
.app-container {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
}

main {
  flex: 1;
}
</style>
